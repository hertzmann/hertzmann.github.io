---
layout: page
title: How to Draw Pictures: Style summary: A non-technical introduction to non-photorealistic rendering, part 3
author:  AaronHertzmann
image: /images/cvpr-gfx.jpeg
date: 2020-09-14
---


# How to Draw Pictures, Part 3: Style



[In two previous blog posts](https://aaronhertzmann.com/2020/09/13/2020-09-12-how-to-draw-pictures-contours.html), I described simple models for drawing. So far, these drawings were relatively plain. But, we can expand on the basic techniques to get a really broad and expressive range of artistic rendering styles.

Stroke style
------------

As already shown, we can use different styles of outline strokes, which includes both drawing brush textures, as well as changing the shapes of the outlines. We can even animate them. Here’s an example of applying different kinds of strokes to animations of 3D models:

<center><iframe src="https://player.vimeo.com/video/45851544" width="640" height="480" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
<p><i>Skip to 4:15 in the video to see stylized 3D stroke animation</i></p></center>


Shading and Hatching
--------

Of course, we might draw inside the shapes. The most popular and well-known non-photorealistic shading algorithm is toon shading, which is widely used in games and animations:

<center>
<figure>
  <img src="../../../images/howtodraw/jet_set_radio.jpeg" alt="Jet Set Radio"/>
  <figcaption align="center"><i>Toon shading in the classic video game Jet Set Radio. Many games and animations use toon shading to give the look of traditional cel animation.
</i></figcaption>
</figure>
</center>
Other notable examples of 3D NPR in video games include [Return of the Obra Dinn](https://en.wikipedia.org/wiki/Return_of_the_Obra_Dinn), [Ōkami](https://en.wikipedia.org/wiki/%C5%8Ckami), [Team Fortress 2](http://www.pixelmaven.com/jason/articles/NPAR07_IllustrativeRenderingInTeamFortress2.pdf), [Borderlands 2](https://en.wikipedia.org/wiki/Borderlands_2), and [Valorant](https://technology.riotgames.com/news/valorant-shaders-and-gameplay-clarity).

But there are lots of other ways to draw objects. For example, hatching is widely used in pencil and pen illustration. Here are the results of an algorithm that we developed to draw hatching illustrations:
<center>
<figure>
  <img src="../../../images/howtodraw/cupid_hatch.png" alt="Cupid hatching"/>
  <figcaption align="center"><i>3D hatching, <a href="https://www.mrl.nyu.edu/publications/illustrating-smooth/">automatically generated</a> from the 3D model on the left.
</i></figcaption>
</figure>
</center>

In order to hatch a surface, we need to determine the hatching directions, as well as their density. In the above illustration, the density is based on a shading: darker regions have cross-hatching. To determine the directions, we notice from looking at real drawings that people often draw lines along the directions in which the surface curves the most and the least (formally, these are called the *principal curvature directions*). Perceptual psychologists have also found that, in isolation, [people tend to perceive hatch lines as curvature directions](https://nyuscholars.nyu.edu/en/publications/observer-biases-in-the-3d-interpretation-of-line-drawings).
We can also let a user author the rendering style. Here is an animation method that applies the [Image Analogies](https://research.adobe.com/image-stylization-history-and-future-part-2/) approach to 3D animation:

<center>
<iframe src="https://player.vimeo.com/video/64407522" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
<p><i>Stylizing Animation By Example</a></i></p></center>

There are lots of other ways to draw objects, whether watercolor, oil; more or less “impressionistic,” and so on.

Most computer animation and games that build on these techniques are essentially creating new visual artistic styles, mashing-up conventional line drawing and painting with computer graphics algorithms. An example is the lovely Paperman animation, which combines contour tracking and toon shading—driven by an enormous amount of authoring and creativity from by professional animators:

<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/mM6cLnscmO8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

Pictorial design
----

All of these rendering styles so far are still relatively “rigid:” they carefully draw each line exactly where linear perspective projection says it should be. However, artists do not normally draw in linear perspective, and sometimes they play with perspective to dramatic effect. Here is a 1914 painting by Giorgio de Chirico, which uses multiple perspectives to give a sense of dissonance and melancholy, and a 3D rendering inspired by it:
<center>
<figure>
  <img src="../../../images/howtodraw/agrawala_perspective.png" alt="Chirico renderings"/>
  <figcaption align="center"><i>Left: 1914 painting by Giorgio de Chirico. Right: 3D rendering by Maneesh Agrawala et al.</i></figcaption>
</figure>
</center>


The 3D rendering on the right uses different camera projections for the three separate objects, violating conventional linear perspective.
Many other elements of drawing and rendering depend on their appearance in the image. For example, this method for Dr. Seuss-style rendering adapts the density of image elements to image space, and makes sure they always face the viewer:
<center>
<figure>
  <img src="../../../images/howtodraw/seuss.png" alt="Seuss rendering"/>
  <figcaption align="center"><i>Dr. Seuss-style rendering (on right) based on the 3D model on the left, by [Kowalski et al.](http://graphics.cs.brown.edu/research/art/)
</i></figcaption>
</figure>
</center>
Here is [a video of that system in action](http://graphics.cs.brown.edu/research/art/kowalski.qt) (albeit low-resolution, and suffering from video transfer artifacts).

Defining Style and the Science of Art
---

The main motivation for this research has been to create new tools for artists. However, the algorithms I’ve described in these blog posts also provide a generative theory for representational art. The more different styles they can create, starting from a relatively small set of concepts — such as contours, stroke styles, and shading styles—the more they could potentially provide a scientific description of how we draw and paint. Furthermore, these building blocks of strokes, shading, and pictorial styles provide a useful way to categorize and understand artistic style.

Despite all these successes so far, there remain many open research problems. How do we programmatically [define the space of styles](http://freestyle.sourceforge.net/), and there are still significant new technologies needed? What [user interfaces](https://gfx.cs.princeton.edu/pubs/Kalnins_2002_WND/index.php) can we use to author styles? Can we combine these techniques with [machine learning](https://people.cs.umass.edu/~dliu/projects/NeuralContours/) and [style transfer](https://dcgi.fel.cvut.cz/home/sykorad/ebsynth.html)?

For a longer discussion of how these models can help create a science of art, see [my NPAR 2004 paper](http://www.dgp.toronto.edu/~hertzman/ScienceOfArt/), and, as well, for how they can help us classify and define style, see [this 2005 paper by Willats and Durand](https://link.springer.com/content/pdf/10.1007/s10516-004-5449-7.pdf).

These generative models are only half of the whole story. To really understand the science of art, we also need to study the visual perception of art. I’ll discuss this topic in a future series of blog posts.
