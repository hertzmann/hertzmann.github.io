---
layout: page
title: "Perspective Distortions: Why Normal Cameras Make Faces Look Weird"
summary: How linear perspective distorts pictures.
author:  AaronHertzmann
image: "/images/perspective/faces_basketballs.jpg"
og:image: "/images/perspective/faces_basketballs.jpg"
---


# Perspective Distortions: Why Normal Cameras Make Faces Look Weird


Have you ever noticed how peoples' faces look stretched in group selfies? 

<center>
<figure>
   <img src="../../../images/perspective/shih_sig19_lowres3.jpg" alt="Wide-angle group selfie?"/>
  <figcaption align="center"><i>Photo by <a href="https://people.csail.mit.edu/yichangshih/wide_angle_portrait/">Shih et al.</a></i></figcaption>
</figure>
</center>

For comparison, here's a more-normal looking picture of the fellow in the lower-right:
<center>
<figure>
   <img src="../../../images/perspective/shih_sig19_lowres3_stereo_crop.jpg" alt="Stereographic projection of a face from the first photo"/>
</figure>
</center>

It's not a flaw in the camera or the lenses—they're operating the way as designed.  

These phenomena come from the use of **[linear perspective](https://en.wikipedia.org/wiki/Perspective_(graphical))** to make pictures.  Linear perspective comes from the Italian Renaissance—and, for the 500 years since then, people have been using it to make pictures, and puzzling over the surprising effects it creates.  

This post explains some of these stretched and misleading faces.  The same principles apply to all kinds of shapes, not just faces though.

This post is based on two chapters of this paper:

| A. Hertzmann. Toward a Theory of Perspective Perception in Pictures. _Journal of Vision_. April 2024, 24(4). \[[Paper](https://jov.arvojournals.org/article.aspx?articleid=2793609)\] \[[Webpage](https://www.dgp.toronto.edu/~hertzman/perspective/)\]  |

# Linear perspective

In the 15th century, Fillipo Brunelleschi and others came up with [**linear perspective**](https://en.wikipedia.org/wiki/Perspective_(graphical)), a technique for drawing pictures.  Here's a modern demonstration of drawing a picture with linear perspective, by placing down vanishing points (the push-pins), and drawing straight lines to the vanishing points:

<center>
   <figure>
<video width="50%" height="50%" controls>
  <source src="../../../images/perspective/Rafael Araujo-3VP-perspective.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
<figcaption><i>Perspective drawing demo by <a href="https://www.rafael-araujo.com/">Rafael Araujo</a></i></figcaption></figure>
</center>

Here's a 16th-century diagram of the principles behind it:

<center>
<img src="../../../images/perspective/perspective_vignola.jpg">
<figcaption><i>Illustration by Giacomo Barozzi da Vignola, 1583</i>
</figcaption>
</center>

The idea of linear perspective is to draw, or measure, the light that hits the viewer's eye, and intersecting the image plane. In the diagram above, the viewer should see the same thing whether they're looking at the picture, or if you removed the picture and looked at the hexagonal object directly.

All the lines of light rays converge at a point called the **center-of-projection (COP)**, or _focal center_.  In this diagram, the COP is where the viewer's eye is.  The above illustration is a little unusual—normally the COP is in front of the middle of the picture.

Linear perspective became a foundational technique for making art, but also came to represent a philosophical ideal: art as a rational process, and a metaphor for rational scientific understanding in general.  And, centuries later, many artists of the Modern Art movement rebelled against it, rejecting linear perspective as they rejected Enlightenment rationality. 

Nonetheless, linear perspective—and its supposed rationality—dominate both our discussions of pictures, and our techniques for making them. Our smartphones and consumer cameras have all sorts of complex optics and fancy shooting modes, but, most of the time, most of us take pictures with cameras that mimic linear perspective.  

I learned linear perspective drawing in a 9th-grade drafting class,  I learned mathematical versions in my undergraduate computer graphics course, and then I taught it when I taught undergraduate computer graphics.   Like many teachers, I taught linear perspective as though it were the "correct" or "default" way to think analytically about making pictures.

(To see why a sphere becomes stretched out like this in linear perspective requires working through the geometry. If you're inclined to try it, trace out the shape of a sphere seen in the corner of a picture. Connecting the silhouette of a sphere to the COP produces a 3D cone that's skewed toward the image corner. Intersecting this cone with the image plane produces an ellipse. One other surprising thing to notice: a flat disc that's parallel to the image plane projects to a circle; the shape must have some depth variation to become distorted.)

# Marginal Distortion 

Modern cameras create linear perspective pictures, but they do it by measuring light rather than drawing lines.  

But linear perspective pictures can make things look distorted. Here's a picture of two of my patient colleagues, taken with my iPhone in ultrawide (0.5x) mode:

<center>
   <figure>
      <img src="../../../images/perspective/faces_basketballs.jpg" alt="Photo of two people and basketballs illustrating marginal distoriton in picture corners">
   </figure>
</center>

Notice how the face and the basketball at the center of the picture look normal, but the face and basketball in the corners look stretched. This is called _marginal distortion_. This is not a flaw of camera optics: marginal distortion occurs with perfect linear perspective. 

I took this picture zoomed out (ultrawide), but the same marginal distortions happen in the smartphone's default mode. 

People have known about marginal distortions for ever since the Renaissance, and puzzled over them. How can it be that the "correct" way to make pictures does such weird things?

(By the way, the term "distortion" is often used to describe deviations from linear perspective, that is, "optical distortion." I do not use it in the way here, as I am writing solely about how pictures are perceived.)



# COP viewing 

In principle, linear perspective requires you to have only one eye open, and to have it located right at the COP, in order for the picture to "look right."

When Leonardo da Vinci first learned about linear perspective, he wrote that a picture will "look wrong" unless the spectator's eye is "at the very distance and height and direction" where the artist's eye had been.

Yet, pictures can "look right" from many different viewpoints. When you view the pictures on this page, or looking at pictures on your phone, you look from many different viewpoints, without taking care to put one eye in just the right spot.

Indeed, doing so would often be quite hard.  Where do you even suppose that a picture's COP is?  Before I started studying this, I had no idea.

Here's that picture again, with a magenta cross to show where the picture's center is:

<center>
   <figure>
      <img src="../../../images/perspective/faces_basketballs_cross.jpg"  alt="Photo of two people and basketballs illustrating marginal distortion in picture corners">
   </figure>
</center>

If you display the picture on a large monitor, and move a smartphone camera to the COP location, then it looks like this:

<center>
   <figure>
<video width="75%" height="75%" controls>
  <source src="../../../images/perspective/COP-viewing.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</figure>
</center>

For this picture, the COP distance is 40% of the width of the picture. So if it appears 5 inches wide on your screen, then your eye should be 2 inches in front of the cross to view it from the COP. If you are reading this on a cell phone, then viewing from the COP is basically impossible because your eye would have to be too close to the screen to be able to see anything.

In short, viewing pictures the way you're "supposed to" is actually very unusual, or sometimes even impossible, for these kinds of _wide-angle_ pictures. And most of the pictures we look at these days are wide-angle. Smartphones take wide-angle photos by default.

**You can try it yourself:** display the picture on a large monitor, and locate the COP, which is in front of the magenta cross, at a distance equal to 40% of the picture's width. Then place your smartphone's camera there, and notice how the picture changes as you move your camera around.  

You can then do it with your eyes. Put one eye where your smartphone camera was, and close the other eye. Again, the marginal distortion should go away.

But, there's a surprise: if you open both eyes, then the marginal distortion reappears. The conventional wisdom says this shouldn't happen.

(The exception are for viewers who are stereoblind, meaning that they do not have normal stereo vision. A stereoblind colleague told me that he does not notice a different with one eye open or with both. Roughly 10% of the population is stereoblind, and many people who are stereoblind do not even realize it.)



# You don't always notice it

We don't always notice this effect, and it can make pictures misleading.

Here's a wide-angle self-portrait by four psychology researchers:

<center>
   <figure>
      <img src="../../../images/perspective/koenderink-military-order-color-crop.jpg">
      <figcaption><i>Wide-angle group self-portrait from <a href="https://journals.sagepub.com/doi/10.1068/p6530">Koenderink et al.</a></i>
      </figcaption>
   </figure>
</center>

How are they facing with respect to each other? Are they parallel, or facing apart?  
My first impression, when looking at the picture, is that they are facing apart from each other. However, they are actually parallel, in this configuration:


<center>
      <img src="../../../images/perspective/koenderink-visual-rays-are-parallel-diagram.jpg">
</center>
With a bit of thought, you can figure this out. Whenever I've shown this picture in technical talks, and asked the audience how the people are facing, someone always responds correctly that they're facing apart. But I don't think it's obvious.


# Pixel correction

I plan to talk about techniques for removing distortion in a future blog post, but I'll mention one here, because you might see it if you take ultrawide portraits on a Pixel or Samsung phone.

Here's a picture taken by one of my colleagues, using a Google Pixel phone in ultrawide mode.  His face appears in the corner, but it's not distorted; why not?

<center>
   <figure>
         <p float="left">
   <img src="../../../images/perspective/andrew-string.jpg" alt="Wide-angle portrait in Google Pixel"  width="40%" height="40%"/>&nbsp;<img src="../../../images/perspective/andrew-string-zoom.jpg" alt="Crop on the face" width="40%" height="40%"/>
</p>
      <figcaption><i>Photo by Elena Adams</i>
      </figcaption>
   </figure>
</center>

The reason is that the Google Pixel automatically applies a correction: it detects faces in the corners of ultrawide pictures, and applies a nonlinear projection for the face, which it blends with the rest of the picture. In this picture, notice how the straight lines (the string and the lines on the wall) have become bent as a result of this blending.  [Their technique](https://people.csail.mit.edu/yichangshih/wide_angle_portrait/) extends a long line of previous distortion-correction techniques, but that's a separate topic (which I may come back to in another blog post).  

I've seen some evidence that Samsung phones all silently do a similar correction for faces, sometimes with rather poor results.


# Perspective expansion and compression

Wide-angle pictures can create various other kinds of distortions. Here are two pictures of a dog that I took moments apart, with the same default iPhone camera settings:

<center>
   <figure>
   <p float="left">
   <img src="../../../images/perspective/pico1.jpg" alt="Dog close-up"  width="40%"/>&nbsp;<img src="../../../images/perspective/pico2.jpg" alt="Dog less close" width="40%"/>
</p>
   </figure>
</center>


In the left picture, the dog's snout looks much larger than its body, whereas it doesn't on the right.  Yet, nothing changed, except that the camera is closer to the dog on the left.  This effect is sometimes called, confusingly, "perspective distortion."

This is why people take selfies at arms-length. Here are four photos of the same person:
<center>
<figure>
   <img src="../../../images/perspective/cooper2012_face.jpg" alt="Photo of a person at different focal lengths"/>
  <figcaption align="center"><i>Photos of the same person at different focal lengths, from <a href="https://jov.arvojournals.org/article.aspx?articleid=2192052">Cooper et al. (2012)</a></i></figcaption>
</figure>
</center>
These were photographed from different distances, and zoomed-in accordingly. (This is sometimes called the "dolly-zoom effect," first appearing in the movie Vertigo.). In fact, [one psychology study found](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0045301) that photographing people from different distances could affect how attractive and trustworthy people appeared in the photos.


Conversely, telephoto photography goes the opposite direction, compressing objects next to each other. You may remember misleading pictures like this, early in the COVID pandemic, that made it look like people failing to obey social distancing rules:

<center>
<figure>
   <img src="../../../images/perspective/distancing.jpg" alt="Illustration of misleading depth when queueing in COVID social distancing"/>
  <figcaption align="center"><i><a href="https://www.theguardian.com/australia-news/2020/sep/13/picture-imperfect-why-photos-of-crowded-beaches-may-not-be-what-they-seem">Misleading depth compression in telephoto photography</a></i></figcaption>
</figure>
</center>

Shifting from close-up to telephoto, while moving away from the subject, can create the dolly-zoom effect illustrated [in this video](https://www.youtube.com/embed/u5JBlwlnJX0).




# Artists don't strictly follow it

When linear perspective was invented in the Italian Renassiance, artists quickly adopted it as a technique for painting. It even became emblematic of the new Western Enlightenment rationalism, providing seemingly-objective ways to make pictures.

Yet, artists quickly discovered some of the above problems. Leonardo da Vinci, as he explored it more, began to distinguish between "artificial" linear perspective and "natural" perspective that more accurately depicts how things look. Since then, many famous artists throughout history have mastered linear perspective, discovered its shortcomings, and then taken different approaches to perspective.

In fact, we can see that even famous examples of linear perspective do not actually obey it.

Here's Raphael's famous _The School of Athens_:
<center>
   <figure>
      <img src="../../../images/arthistory/school_of_athens.jpg">
   </figure>
</center>
The architecture strictly follows one-point linear perspective.  But, take a look at the lower-right corner:
<center>
   <figure>
      <img src="../../../images/arthistory/school_of_athens_crop.jpg">
   </figure>
</center>
The faces and spheres do not have any of the marginal distortions that we see in linear perspective.

In all of art history, _I have never seen a linear perspective picture that depicts faces with marginal distortion_, even though there are many, many wide-angle pictures with faces in the margins. This illustrates how rare strict linear perpsective is in art history.

Art historian Martin Kemp surveyed the classical paintings in Oxford's Ashmolean Museum, and found that only 3% of them _strictly_ followed linear perspective construction rules.  He told me that classical painters often used linear perspective to construct architecture like a stage set, and then moved the people around on it freely.

And, throughout art history, we have far more different kinds of pictures, from cave paintings, to ancient Chinese parallel projections, to Russian reverse perspective, and all the different experiments and styles in Modern art and contemporary art and beyond.

Linear perspective is a very powerful and useful technique, but it is just one of many ways to make pictures. In a future blog post I'll talk about others.





# What's going on here? 

There are two common explanations given for the distortions created by linear perspective. Both are compelling. But, I think, the first one is wrong, and the second is technically true but very misleading.

The first common explanation is that photography with a normal focal length (tehcnically, about 50 mm), "mimics human perception."  This is compelling but doesn't make a whole lot of sense. Photographs don't replace human vision—it's not like pictures bypass your eyes, being directly downloaded into the middle of your brain.  

Instead, photos are a bit more like "virtual reality:" putting something in front of your eyes to replace the real world.  But there's more to it than that. If pictures only worked like virtual reality, then we'd have to view them from the COP.

This leads to the second common explanation: the distortions occur because we're not viewing pictures from the COP. It's true that if we viewed pictures from the COP—with one eye open—we wouldn't see these distortions.  But this just isn't how people look at pictures.  

In fact, in a series of experiments, [Cooper et al. showed](https://jov.arvojournals.org/article.aspx?articleid=2192052) that people tend to view pictures from comfortable viewing distances. We don't get closer or further from pictures based on where the COP is. So, to me, this means that pictures should be made to work well based on where people view them. This often isn't possible with strict linear perspective. 

Throughout art history and perception research, there is a long history of assuming that linear perspective is the "right" way to make pictures, and any distortions or misperceptions must be "user error," i.e., mistakes made by the artist or the brain.  To me, this seems backwards.  If human vision doesn't perceive pictures according to the "rules" of  linear perspective, then the "rules" aren't quite right. 


In a future blog post, I'll describe ways to make pictures that do much better than linear perspective at avoiding distortion. (Until then, see [my paper](https://www.dgp.toronto.edu/~hertzman/perspective).)




<hr>

Thanks to Andrew Adams, Elena Adams, Daniel Martin and Bryan Russell for help with example pictures.


