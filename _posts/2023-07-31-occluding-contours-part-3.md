---
layout: page
title: "Occluding Contour Breakthroughs Part 3: Which Algorithm Should I Use (or Research)?"
summary: Summary of different approaches for different cases, and open questions
author:  AaronHertzmann
image: "/images/howtodraw/howtodraw/spiderverse.jpg"
og:image: "/images/howtodraw/howtodraw/spiderverse.jpg"
---


# Occluding Contour Breakthroughs Part 3: Which Algorithm Should I Use (or Research)?

_This blog post has now been revised and adapted into a paper. Please cite the paper where appropriate:_

* A. Hertzmann, "New Insights in Smooth Occluding Contours for Nonphotorealistic Rendering" in IEEE Computer Graphics and Applications, vol. 44, no. 01, pp. 76-85, 2024. \[[Paper (open access)](https://www.computer.org/csdl/magazine/cg/2024/01/10414224/1TZIQ9i1pvy)\]

_In addition, **the paper includes a new section** summarizing different classes of approaches that work for this problem._

<hr>

Suppose you want to compute occluding contours of a smooth surface. Given the literature out there, and [the new developments summarized in my previous blog post](/2023/07/31/occluding-contours-part-2.html), which method should you use? And, where is more research needed?  On this page, I'll summarize my opinions on these questions.

In most cases, I'll assume you're starting with a triangle mesh, or you're willing to convert your input to a triangle mesh.   

<p><center><b><u>
I just want simple solid lines.
</u></b></center></p>

For this case, you can just use an edge-detection shader, as has been used in many movies and [video games](http://www.cs.williams.edu/~morgan/SRG10).  See
 Chapter 2 of [our tutorial](https://arxiv.org/abs/1810.01175) for more detail.

<center>
<figure>
  <img src="../../../images/howtodraw/spiderverse.jpg" alt="Spiderverse image"/>
  <figcaption align="center"><i>The character on the left has occluding contour outlines.
</i></figcaption>
</figure>
</center>

<p><center><b><u>
I want stylized vector curves, but they don't need to be robust or topologically-valid.
</u></b></center></p>

If you want smooth strokes, but you're willing to accept some amount of gaps and flickering in your curves, then there are a wealth of existing methods; see Chapters 5 and 6 of [our tutorial](https://arxiv.org/abs/1810.01175). As a starting point, I'd recommend [our interpolation algorithm](https://mrl.cs.nyu.edu/publications/illustrating-smooth/), summarized in Section 6.2 of the tutorial; it's the same one used in Blender Freestyle. If you want faster performance, [this recent GPU paper](https://github.com/JiangWZW/Realtime-GPU-Contour-Curves-from-3D-Mesh) may be worth a look.

With clever heuristics, you can improve these results to reduce the amount of flickering, and the occasional gaps that appear in curves that should be solid. But you will never, never get rid of them completely.

<center>
<figure>
  <img src="../../../images/howtodraw/cupid_hatch.png" alt="Cupid hatching"/>
  <figcaption align="center"><i>3D hatching, <a href="https://www.mrl.nyu.edu/publications/illustrating-smooth/">automatically generated</a> from the 3D model on the left.
</i></figcaption>
</figure>
</center>

<p><center><b><u>
I want topologically-valid smooth curves.
</u></b></center></p>

If you want curves that are topologically-valid, and thus can animate without unnecessary flickering, and can be vectorized into closed regions, then I believe the state-of-the-art is our new [quadratic contours method](http://ryanjcapouellez.com/papers/algebraic_smooth_occluding_contours.html).

There are two caveats with this method. First, like any newly-published research paper, it's hard to know if it's robust enough for production; perhaps numerical errors do cause problems in some cases, even though we didn't see it in our testing. Second, the algorithm is fairly involved to understand. [The code is online](http://ryanjcapouellez.com/papers/algebraic_smooth_occluding_contours.html), but it might be challenging if you need to implement it yourself or modify it for some reason. 


<p><center><b><u>
I want topological validity and easier implementation, but don't need perfection.
</u></b></center></p>

As discussed in the previous post, planar map methods can guarantee topological validity: compute the planar map of a triangle mesh, and you're guaranteed that the planar map has valid visibility. But you're not guaranteed a nice simple set of curves—there might be superfluous junk, but [such representations can be simplified](http://www.dgp.toronto.edu/~alexk/segegsr.html). I think there's lots of room to develop practical new techniques here; I can imagine several different approaches.



<p><center><b><u>
I want both topological validity <i>and</i> accuracy to a specific smooth surface representation.
</u></b></center></p>

Suppose you have a mathematically-smooth surface, like a subdivision surface, in an engineering or rendering application where accuracy is important. Perhaps you care about getting contours that _precisely_ follow those of the underlying surface, perhaps with some guaranteed accuracy or alignment to another rendering.

This is what [the ConTesse algorithm](https://dgp.toronto.edu/~hertzman/contesse/) can provide for subdivision surfaces (the code is online). And, I think that the strategy in that paper could be applied to any other smooth surface represention (e.g., implicits), with some additional development effort.

However, I think there's lots of room to improve this approach, with more research. This is research code, and we don't know how robust it will be. In theory it will converge for any surface, but it could take ages for complicated cases. See the Discussion section of the paper for much more information and ideas. Perhaps, with enough effort, this approach could be competitive with the quadratic  approach.



<p><center><b><u>
I want more curves besides just occluding contours.
</u></b></center></p>

Occluding contours are just the starting point: there's a [wealth of stylization options](/2020/09/14/how-to-draw-pictures-style.html). For visibility, there are few curves you need to get right: occluding contours, boundaries, and surface self-intersections. Then, one can add all sorts of wonderful and artistic stylizations.

All of these steps are conceptually straightforward exensions of the above contour algorithms. But actually implementing them may be involved, and there may be more research to do to work out the details, e.g., how do you handle self-intersecting surfaces in these representations.

<p><center><b><u>
I want to help artists make cool art and animation
</u></b></center></p>

These algorithms provide a foundation for artistic tools for animation. Here's a video from [a 2002 paper that I still find inspirational](https://gfx.cs.princeton.edu/pubs/Kalnins_2002_WND/index.php):

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/gT9qU_fJNuw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</center>

Related techniques [were used in Disney's Paperman](https://www.youtube.com/watch?v=TZJLtujW6FY) and the Spider-Verse movies.  But now, with working occluding contour algorithms, we could make these techniques so much better.

The [Freestyle Paper](https://dl.acm.org/doi/abs/10.1145/1731047.1731056) illustrates a second approach to authoring many artistic styles on top of these representations, i.e., writing procedural "shaders".

Finally, we could also use machine learning on top of these representations, [as illustrated in our Neural Strokes paper](https://people.cs.umass.edu/~dliu/projects/NeuralStrokes/), thereby providing some of the best of both worlds: the guaranteed control and precision of geometric computation, with the stylistic range and expressivity of ML-based methods.
