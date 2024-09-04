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
With a bit of thought, you can figure this out. Whenever I've shown this picture in technical talks, and asked the audience how the people are facing, someone always responds correctly that they're parallel. But I don't think it's obvious.


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

<center>
<blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/CoVIl19DxN5/?utm_source=ig_embed&amp;utm_campaign=loading" data-instgrm-version="14" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:540px; min-width:326px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:16px;"> <a href="https://www.instagram.com/reel/CoVIl19DxN5/?utm_source=ig_embed&amp;utm_campaign=loading" style=" background:#FFFFFF; line-height:0; padding:0 0; text-align:center; text-decoration:none; width:100%;" target="_blank"> <div style=" display: flex; flex-direction: row; align-items: center;"> <div style="background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 40px; margin-right: 14px; width: 40px;"></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 100px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 60px;"></div></div></div><div style="padding: 19% 0;"></div> <div style="display:block; height:50px; margin:0 auto 12px; width:50px;"><svg width="50px" height="50px" viewBox="0 0 60 60" version="1.1" xmlns="https://www.w3.org/2000/svg" xmlns:xlink="https://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(-511.000000, -20.000000)" fill="#000000"><g><path d="M556.869,30.41 C554.814,30.41 553.148,32.076 553.148,34.131 C553.148,36.186 554.814,37.852 556.869,37.852 C558.924,37.852 560.59,36.186 560.59,34.131 C560.59,32.076 558.924,30.41 556.869,30.41 M541,60.657 C535.114,60.657 530.342,55.887 530.342,50 C530.342,44.114 535.114,39.342 541,39.342 C546.887,39.342 551.658,44.114 551.658,50 C551.658,55.887 546.887,60.657 541,60.657 M541,33.886 C532.1,33.886 524.886,41.1 524.886,50 C524.886,58.899 532.1,66.113 541,66.113 C549.9,66.113 557.115,58.899 557.115,50 C557.115,41.1 549.9,33.886 541,33.886 M565.378,62.101 C565.244,65.022 564.756,66.606 564.346,67.663 C563.803,69.06 563.154,70.057 562.106,71.106 C561.058,72.155 560.06,72.803 558.662,73.347 C557.607,73.757 556.021,74.244 553.102,74.378 C549.944,74.521 548.997,74.552 541,74.552 C533.003,74.552 532.056,74.521 528.898,74.378 C525.979,74.244 524.393,73.757 523.338,73.347 C521.94,72.803 520.942,72.155 519.894,71.106 C518.846,70.057 518.197,69.06 517.654,67.663 C517.244,66.606 516.755,65.022 516.623,62.101 C516.479,58.943 516.448,57.996 516.448,50 C516.448,42.003 516.479,41.056 516.623,37.899 C516.755,34.978 517.244,33.391 517.654,32.338 C518.197,30.938 518.846,29.942 519.894,28.894 C520.942,27.846 521.94,27.196 523.338,26.654 C524.393,26.244 525.979,25.756 528.898,25.623 C532.057,25.479 533.004,25.448 541,25.448 C548.997,25.448 549.943,25.479 553.102,25.623 C556.021,25.756 557.607,26.244 558.662,26.654 C560.06,27.196 561.058,27.846 562.106,28.894 C563.154,29.942 563.803,30.938 564.346,32.338 C564.756,33.391 565.244,34.978 565.378,37.899 C565.522,41.056 565.552,42.003 565.552,50 C565.552,57.996 565.522,58.943 565.378,62.101 M570.82,37.631 C570.674,34.438 570.167,32.258 569.425,30.349 C568.659,28.377 567.633,26.702 565.965,25.035 C564.297,23.368 562.623,22.342 560.652,21.575 C558.743,20.834 556.562,20.326 553.369,20.18 C550.169,20.033 549.148,20 541,20 C532.853,20 531.831,20.033 528.631,20.18 C525.438,20.326 523.257,20.834 521.349,21.575 C519.376,22.342 517.703,23.368 516.035,25.035 C514.368,26.702 513.342,28.377 512.574,30.349 C511.834,32.258 511.326,34.438 511.181,37.631 C511.035,40.831 511,41.851 511,50 C511,58.147 511.035,59.17 511.181,62.369 C511.326,65.562 511.834,67.743 512.574,69.651 C513.342,71.625 514.368,73.296 516.035,74.965 C517.703,76.634 519.376,77.658 521.349,78.425 C523.257,79.167 525.438,79.673 528.631,79.82 C531.831,79.965 532.853,80.001 541,80.001 C549.148,80.001 550.169,79.965 553.369,79.82 C556.562,79.673 558.743,79.167 560.652,78.425 C562.623,77.658 564.297,76.634 565.965,74.965 C567.633,73.296 568.659,71.625 569.425,69.651 C570.167,67.743 570.674,65.562 570.82,62.369 C570.966,59.17 571,58.147 571,50 C571,41.851 570.966,40.831 570.82,37.631"></path></g></g></g></svg></div><div style="padding-top: 8px;"> <div style=" color:#3897f0; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:550; line-height:18px;">View this post on Instagram</div></div><div style="padding: 12.5% 0;"></div> <div style="display: flex; flex-direction: row; margin-bottom: 14px; align-items: center;"><div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(0px) translateY(7px);"></div> <div style="background-color: #F4F4F4; height: 12.5px; transform: rotate(-45deg) translateX(3px) translateY(1px); width: 12.5px; flex-grow: 0; margin-right: 14px; margin-left: 2px;"></div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(9px) translateY(-18px);"></div></div><div style="margin-left: 8px;"> <div style=" background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 20px; width: 20px;"></div> <div style=" width: 0; height: 0; border-top: 2px solid transparent; border-left: 6px solid #f4f4f4; border-bottom: 2px solid transparent; transform: translateX(16px) translateY(-4px) rotate(30deg)"></div></div><div style="margin-left: auto;"> <div style=" width: 0px; border-top: 8px solid #F4F4F4; border-right: 8px solid transparent; transform: translateY(16px);"></div> <div style=" background-color: #F4F4F4; flex-grow: 0; height: 12px; width: 16px; transform: translateY(-4px);"></div> <div style=" width: 0; height: 0; border-top: 8px solid #F4F4F4; border-left: 8px solid transparent; transform: translateY(-4px) translateX(8px);"></div></div></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center; margin-bottom: 24px;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 224px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 144px;"></div></div></a><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/reel/CoVIl19DxN5/?utm_source=ig_embed&amp;utm_campaign=loading" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">A post shared by Alex Harrison (@harrison)</a></p></div></blockquote> <script async src="//www.instagram.com/embed.js"></script>
</center>

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

(What's more, none of the art historians or perceptual psychologists I've read seem to have noticed this discrepancy; they sometimes say that Raphael has perfectly followed linear perspective everywhere but the spheres.) 

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


