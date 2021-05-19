---
layout: page
summary: A non-technical introduction to non-photorealistic rendering, part 2
author:  AaronHertzmann
image: /images/howtodraw/abstracted_shading.png
---


# How to Draw Pictures, Part 2: Suggestive Contours


In [the first part of this series](/2020/09/12/how-to-draw-pictures-contours.html), I described Occluding Contours, which are the fundamental building blocks of line drawing. Now I will describe an important extension to them, and discuss what these theories tell us about how people make line drawings.

Abstracted shading
----------------
Here’s a different interpretation of contours, this time based on shading. This shading interpretation is a little more subtle, but leads to important insights.

We start with a 3D model. In this example, I’ll start with a 3D model of a cow. Let’s paint the cow with matte white paint, and place it in a white room. We’ll photograph it with no lighting other than a headlamp sitting atop the camera. We take a picture with the camera, and it looks like this:
<center>
<figure>
  <img src="../../../images/howtodraw/cow_diffuse.png" alt="Diffuse cow"/>
  <figcaption align="center"><i>Matte rendering of a cow, lit from the camera position. In computer graphics terminology, this is a white surface rendered with Lambertian shading, without non-local effects like interreflections or cast shadows. (Image created by Pierre Bénard using <a href="https://github.com/fcole/qrtsc">qrtsc</a>.)
</i></figcaption>
</figure>
</center>


The pixels in this image range from white to gray to black. If the draw lines through just the completely black pixels in this image, we get the contours:
<center>
<figure>
  <img src="../../../images/howtodraw/cow_contours.png" alt="Cow contours"/>
  <figcaption align="center"><i>Contour curves on the cow, without any stylization. (Image created by Pierre Bénard using <a href="https://github.com/fcole/qrtsc">qrtsc</a>.)
</i></figcaption>
</figure>
</center> 
If we draw lines through not just the black pixels but also the darkest regions of this image, then we get this drawing:
<center>
<figure>
  <img src="../../../images/howtodraw/cow_sc.png" alt="Cow contours"/>
  <figcaption align="center"><i> Contour and Suggestive Contour curves on the cow, without any stylization. (Image created by Pierre Bénard using <a href="https://github.com/fcole/qrtsc">qrtsc</a>.)
</i></figcaption>
</figure>
</center> 
This image includes both the contours, and a new set of curves called the *suggestive contours*. The suggestive contours were first introduced in [a beautiful paper that analyzed their mathematical and geometric properties in considerable depth](https://gfx.cs.princeton.edu/proj/sugcon/), 
and [formulated as abstracted shading by Lee et al.](https://dl.acm.org/citation.cfm?id=1276377.1276400), for example:
<center>
<figure>
  <img src="../../../images/howtodraw/abstracted_shading.png" alt="Abstracted shading"/>
  <figcaption align="center"><i> Real-time abstracted shading rendering of 3D models, from <a href="https://dl.acm.org/citation.cfm?id=1276377.1276400">a 2007 paper by Lee et al.</a>
</i></figcaption>
</figure>
</center> 
(Incidentally, [a much earlier image processing paper formulated the same basic idea as well](https://ieeexplore.ieee.org/abstract/document/1457470).)
This idea of making drawings by approximating a shaded rendering with strokes can also be extended to determine stroke thickness, for example:
<center>
<figure>
  <img src="../../../images/howtodraw/thick_strokes.png" alt="Thick stroke renderings"/>
  <figcaption align="center"><i>Rendering with contours and suggestive contours, and stroke thickness based on shading (from <a href="http://www.dgp.toronto.edu/~todd/isophote/">our 2007 paper on stroke thickness</a>.
</i></figcaption>
</figure>
</center>

Here's [a separate blog post about the line thickness algorithm](/2021/05/20/how-to-draw-pictures-line-thickness.html).

Scientific evaluation
--------------

<center>
<figure>
  <img src="../../../images/howtodraw/cole_study.png" alt="Drawing study"/>
  <figcaption align="center"><i>In this study, artists were asked to make line drawings of 3D models.
</i></figcaption>
</figure>
</center> 

The above explanation of line drawings is a very simple, compact theory of line drawings. How well does it really predict real line drawings?
A [rigorous study was conducted by Forrester Cole and his collaborators](https://gfx.cs.princeton.edu/pubs/Cole_2008_WDP/index.php). They asked 29 artists to create line drawings from 3D renderings. They found that the lines that artists drew agreed with the predictions of existing line drawing algorithms most of the time. Specifically, image shading gradients were the most reliable predictor of artists’ drawings, since these objects had more complex shading than the model I described above. The shading gradients basically correspond to the curves described above. The cases where they disagreed were subtle, for example, the artists omitted curves that could be inferred by understanding the overall shape of the rest of the object.

Conclusion
----------
As outlined here, the theory of contours and suggestive contours is a simple and compact theory that explains a lot of the way that we draw lines. Understanding this theory ought to be foundational for anyone that wishes to understand the basic mechanics of representational art.

In [the next essay in this series](/2020/09/14/how-to-draw-pictures-style.html), I’ll talk about how these basic foundations can be used to describe many different artistic styles.
