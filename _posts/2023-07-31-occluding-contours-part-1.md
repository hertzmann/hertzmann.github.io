---
layout: page
title: "Occluding Contour Breakthroughs, Part 1: A Surprisingly Hard Problem"
summary: Exact line rendering of smooth surfaces is harder than anyone would think
author:  AaronHertzmann
image: "/images/howtodraw/cupid_hatch.png"
og:image: "/images/howtodraw/cupid_hatch.png"
---


# Occluding Contour Breakthroughs, Part 1: A Surprisingly Hard Problem


The [occluding contours of a smooth surface](/2020/09/12/how-to-draw-pictures-contours.html) let you render 3D objects [in many different artistic styles](/2020/09/14/how-to-draw-pictures-style.html), such as this pen-and-ink hatching style:

<center>
<figure>
  <img src="../../../images/howtodraw/cupid_hatch.png" alt="Cupid hatching"/>
  <figcaption align="center"><i>3D hatching, <a href="https://www.mrl.nyu.edu/publications/illustrating-smooth/">automatically generated</a> from the 3D model on the left.
</i></figcaption>
</figure>
</center>
Simple occluding contour renderings appear throughout many kinds of animations, TV shows and films throughout the past few decades, often consisting of basic black outlines. 
Some recent examples include [the game "Hi-Fi Rush"](https://www.youtube.com/watch?v=pgd4aU56Kig)
and the Spider-Verse movies:
<center>
<figure>
  <img src="../../../images/howtodraw/spiderverse.jpg" alt="Spiderverse image"/>
  <figcaption align="center"><i>The character on the left has occluding contour outlines.
</i></figcaption>
</figure>
</center>

Now, there are a lot richer classes of stylizations in the research literature. Here are some examples:
<center>
<figure>
  <img src="../../../images/howtodraw/styles.jpg" alt="NPR contour styles"/>
</figure>
</center>
But we're not seeing these styles in games or movies. Why not? These styles rely on vector contour extraction algorithms, and all of the existing algorithms for smooth surfaces have unpredictable failure cases. And we've never really understood why.  

This year, we finally cracked the case. 

In a paper called [ConTesse](https://dgp.toronto.edu/~hertzman/contesse/), we finally explain exactly what the problem really is, and describe when a solution works or doesn't; moreover, we describe a method that produces correct results for subdivision surfaces. And, in [a second paper](http://ryanjcapouellez.com/papers/algebraic_smooth_occluding_contours.html), we show
how to generate exact smooth contours based on input meshes, allowing for very fast and accurate contours.

In this blog post, I explain exactly what the problem is, and, in [the next post](/2023/07/31/occluding-contours-part-2.html), what the breakthroughs are. In [the third post](/2023/07/31/occluding-contours-part-3.html), I recommend which of the existing methods to try for different types of problems, and point to where more research and development is needed to move these ideas from research to practical applications.


This post is intended for readers knowledgable about computer graphics algorithms. You can find [a non-technical introduction to these topics here](/2020/09/12/how-to-draw-pictures-contours.html).  


# The Occluding Contour Problem

Here's an example of occluding contours, drawn as black lines on a 3D model:

<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/pig_toon.png" alt="Occluding contour rendering" width="60%"/>
</p>
</figure>
</center>

The occluding contours occur where a surface overlaps itself in image space:

<center>
<figure>
   <p float="left">
   <img src="../../../images/howtodraw/pig_side.png" alt="Contour defintions"  width="60%"/>
</p>
</figure>
</center>

For a triangle mesh, it's easy to find the occluding contours: take all the edges that connect a front-face to a back-face, and then compute which of those edges are visible:

<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/mesh-contour-def.png" alt="Occluding contours for meshes" width="80%"/>
</p>
</figure>
</center>
Our existing algorithms for triangle mesh contours are robust and effective.

I'm assuming that the surface is _oriented_: the faces have normal directions consistent with their neighbors, and the camera position is constrained, so that only front-facing surface will ever be visible. These assumptions are common in computer graphics applications.


(In this post, I am being very casual with definitions and terminology.  You can see [our tutorial paper for a detailed and precise definitions](https://arxiv.org/abs/1810.01175).)


**For smooth surfaces,** i.e., surfaces with continous normals, the occluding contours are all _visible_ surface points where _the tangent plane contains the view vector_. For example:

<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/smooth-contour-def.png" alt="Occluding contours for meshes" width="80%"/>
</p>
</figure>
</center>

That shouldn't be so hard to compute, right?


# Topology Problems

What makes the problem difficult isn't computing the contour points, it's computing the _visible_ points. We want the visible curves to have sensible topology: no gaps at all in the outlines, nor extra curves and junctions, or other mistakes that would mess up stylization.  

For example, suppose you start with this smooth object:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/ovoid-smooth.png" alt="Occluding contours for meshes" width="40%"/>
</p>
</figure>
</center>
The obvious thing is to triangulate it into a mesh, and then compute the contours of the mesh. But look what happens:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/ovoid-mesh.png" alt="Occluding contours for meshes" width="40%"/>
</p>
</figure>
</center>
The smooth object has a simple contour, but the triangle mesh's contour has lots of extra complicated pieces. This is because the surface is no longer cleanly split into one front-facing region and one back-facing region.  The simple contour has become a mess, and this gets worse as surfaces get more complicated:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/bunny-purple.png" alt="Occluding contours for meshes" width="60%"/>
</p>
</figure>
</center>
(This is an older rendering with a different color scheme for front and back faces.) 

This matters when you try to stylize the contours, such as this animation:
<center>
<video width="720" height="480"  controls>
  <source src="../../../images/howtodraw/Angela_candle_meshC-17288.mp4" type="video/mp4">
Your browser does not support the video tag.
</video></center>

Note how the stylization flickers and strokes appear and disappear, despite a number of attempts in this algorithm to keep things coherent.


# Really, It's Shockingly Hard

If you are like most researchers, you might think there are simple solutions to this problem. In my experience, pretty much _everyone_, when confronted with these problems, immediately suggests simple solutions that they confidently believe will solve the problem.  

For example, you could come up with [simple rules to fix up the curves](https://www.cs.princeton.edu/courses/archive/fall00/cs597b/papers/artistic-sils-300dpi.pdf), but these will all fail in various ways. You could try subdividing the surface (as did one very confident paper reviewer recently told us), but this doesn't fix anything (we analyzed why [in our 2014 paper](https://www.labri.fr/perso/pbenard/publications/contours/)).  Nothing has worked robustly.  Many other algorithms are surveyed in [our tutorial paper](https://arxiv.org/abs/1810.01175), Chapters 6 and 7.

[We proposed one of these algorithms in our 2001 paper](https://mrl.cs.nyu.edu/publications/illustrating-smooth/), an interpolation-based approach that makes nice smooth curves. But, if you zoom in on the figures, you can see gaps in the outlines:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/cupid-gaps.png" alt="Occluding contours and hatching on a cupid model" width="40%"/>
</p>
</figure>
</center>


And this affects real applications. For example,  [Blender Freestyle](https://en.wikipedia.org/wiki/Freestyle_(software)) uses  our 2001 algorithm, from the implementation in [Stephane Grabli's work](https://dl.acm.org/doi/abs/10.1145/1731047.1731056).  [Online, you can find many complaints about the gaps](https://www.google.com/search?q=freestyle+gaps+blender) in Freestyle's contours:
<center>
<figure>
   <p float="left">
   	<a href="https://blenderartists.org/t/trying-to-close-gaps-in-freestyle-lines/688753">
<img src="../../../images/howtodraw/freestyle.png" alt="Blender forum discussion of gaps in Freestyle" width="60%"/></a>
</p>
</figure>
</center>
And, here's an animation from [a 2011 paper](https://dl.acm.org/doi/10.1145/2024676.2024683) that tries to fix our method using planar maps, but still has gaps in the outline in some frames:

<center>
<video width="640" height="360"  controls>
  <source src="../../../images/howtodraw/karsch-hart-snaxels.mp4" type="video/mp4">
Your browser does not support the video tag.
</video></center>
Even [the pig image](../../../images/howtodraw/pig_toon.png), which we showed in our survey paper, has an incorrect gap that I only just noticed writing this post.

In addition to their effects on animation, gaps and other errors prevent _vectorization_, converting these curves to 2D vector graphics. This is important for region-based stylization, filling regions with styles, since style is not just about outline curves, it's about how you fill in regions as well. 

This problem was [first published in 1966](https://dl.acm.org/doi/abs/10.1145/321328.321330); it's older than photorealistic computer graphics. Depending on how you count, I've spent nearly _a decade_ of my career working on this one little problem (that's [wall-clock time](https://en.wikipedia.org/wiki/Elapsed_real_time), not system time).  You try implementing something, and it seems like there's just one or two cases to fix with heuristics, but then other cases don't work... and it becomes whack-a-mole. Nothing works reliably.

And it wasn't just that we didn't know how to get the curves looking "right", we didn't even know how, exactly, to define the problem... what does "right" even mean here?


# [Read on in Part 2 for some answers](/2023/07/31/occluding-contours-part-2.html)
