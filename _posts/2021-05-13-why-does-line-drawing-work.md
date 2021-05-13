---
layout: page
title: Why Does Line Drawing Work?
summary: A computer graphics model gives insight into human perception of art
author:  AaronHertzmann
image: /images/howtodraw/fox.jpg
---




# Why Does Line Drawing Work? A Realism Hypothesis

This page summarizes my new hypothesis about why line drawings work, which was published in a vision science journal in 2020 and 2021. You can also watch [a presentation of this work on YouTube](https://www.youtube.com/watch?v=FxrwJFjGyP4).  

<p><a href="#citations"><b>Paper links</b></a></p>


**We begin with a mystery.** We have eyes and vision in order to help us navigate and survive in the real world. Evolution gives us abilities to quickly and accurately understand images of the real world. If you see a picture of the forest at night in the fog, you can immediately tell what it is and recognize objects in the scene. Being able to accurately, quickly, and continually understand the world around us helps us find food, avoid danger, and live together with other people.  Mistakes in vision–like hallucinating something that isn't there–can lead to misunderstandings, accidents, or even death.

It's not too surprising that we can understand photographs, since they look a lot like the real world. But what about line drawings? These look nothing like the real world. We don't see black pen outlines walking around on white backgrounds.  Yet, we can understand drawings just as easily as we can understand photographs.  We see shape in drawings rather than just seeing them as marks of ink on a page. Why would this be?

<center>
<img src="https://aaronhertzmann.com/images/howtodraw/fox.jpg" alt="Cartoon fox">
</center>


If you can understand real images, you can understand basic line drawings
=====

[One influential philosophical theory](https://en.wikipedia.org/wiki/Languages_of_Art) holds that all artist styles are learned from our cultures and upbringings.  We learn to understand line drawings when we are children, in the same way that we learn to understand written language. Everything about art is a product of our cultures.

Yet, line drawings exist throughout many different historical cultures, even preceding civilization. Cave paintings made by our prehistoric ancestors using outline drawing and are easily recognizable to us today. Moreover, [numerous studies with members of tribal societies](https://journals.sagepub.com/doi/10.1068/p040391) show that someone who has never seen a picture can understand what's in a line drawing.

A few years ago, I wondered if perhaps understanding line drawing is a consequence of real-world vision. Specifically, I hypothesized that, if we could train a computer vision algorithm to understand 3D shape in real-world imagery just as well as humans, then that algorithm would also be able to understand shape in line drawings.  While our current computer vision algorithms aren't nearly as good as humans, I still thought I'd try it out. I downloaded [a model that was state-of-the-art at the time](https://arxiv.org/abs/1907.01341v1). This deep neural network predicts relative depth for each pixel in a photograph:

![Depth estimation results on photos](/images/howtodraw/midas-real2.jpg)

Importantly, this model was solely trained on photographs, not on drawings. And, when I tried it on some line drawings, I got similar results!

![Depth estimation results on drawings](/images/howtodraw/midas-drawing.jpg)

This shows that perception of line drawing must be somehow a consequence of real-world perception. But why?

(Many vision researchers have informally hypothesized that line drawing perception is a consequence of edge receptors in the early stages of the human vision system, but [I think this is implausible for many reasons.](/2020/04/19/lines-as-edges.html))


Line drawing as Abstracted Shading
=====

It turns out that there's a way to create line drawings that is based on _possible_ real-world conditions.

Set up a 3D object in front of you. Paint it white. Turn off all the light sources, except for a headlamp that you wear on your forehead. If the object is a model of a cow, it may look like this:

<center>
<img src="https://aaronhertzmann.com/images/howtodraw/cow_diffuse-sm.jpg" alt="Diffuse rendering of a cow">
</center>

If we draw a picture of this image with a black pen on white paper, the simplest thing to do is to draw lines through the darkest regions. And that picture might look like this:

<center>
<img src="https://aaronhertzmann.com/images/howtodraw/cow_thick.jpg" alt="Line rendering of a cow">
</center>

We can see that _the drawing is, approximately, a plausible real-world image._ That is, it's not something that we're likely to see around us. But it's something that we _could_ see in the real world... and we are able to understand realistic photos of things we've never seen before-even when the image is corrupted with fog or rain or image noise-and this rendering setup shows how a realistic setup can approximately produce line drawings. [This model of line drawing originated in computer graphics research.](/2020/09/13/how-to-draw-pictures-suggestive-contours.html)

| I hypothesize that, for a person who has never seen a picture before, **the human visual system interprets a line drawing as if it were a realistic image, with a lighting and material setup similar to those above.** |

In other words, the key idea is that, for a line drawing, _there exists_ a realistic interpretation of the line drawing. If you see the image on the right, can interpret it as if it were the image on the left:

![Valleys of a 3D model with glossier materials](/images/howtodraw/ david_valleys.jpg)

This setup works with various different settings of materials and lighting; here are two other possible examples. In each case, the lines are being determined by [a valley-detector algorithm](https://ieeexplore.ieee.org/abstract/document/1457470) (in OpenCV):

![Valleys of a photograph](/images/howtodraw/photo_valleys.jpg)

This hypothesis doesn't say anything about how the vision system actually works. It says that, whatever the vision system is doing for photographs, it's doing basically the same thing for line drawings in the same way.



Future directions
====

This hypothesis could be tested by brain-imaging experiments with human subjects. I predict that the neural responses to a line drawing will be very similar to those of corresponding 3D renderings. There are some previous neuroscience studies that have been performed comparing neural responses of line drawings to photographs; these methodologies could be used to test my predictions. This could also be used to assess what kinds of lighting and material setups best match line drawings.  I don't have the expertise or resources to perform these experiments, though I'd be interested in talking with people who do.

This theory focuses solely on a very basic line drawing style. In the paper, I discuss how several other types of line drawings-such as white-on-black drawing and hatching-can also be understood as abstracted shading. But the range of visual artistic styles we can understand is vast; we seem to have the ability to visually separate style from content. How do we do this?

<a name="citations">

Papers
=====

These ideas were first described in the following paper:

* **A. Hertzmann. Why Do Line Drawings Work? A Realism Hypothesis. _Perception_. 2020. 49(4):439-451.** [Official paper link](https://journals.sagepub.com/doi/abs/10.1177/0301006620908207?journalCode=peca), [arXiv preprint](https://arxiv.org/abs/2002.06260)

The second paper expands on how this hypothesis relates to theories based on edge detection. It is meant to be self-contained, and may be easier to read:

* **A. Hertzmann. The Role of Edges in Line Drawing Perception. _Perception_. 2021. 50(3):266-275.** [Official paper link](https://journals.sagepub.com/doi/abs/10.1177/0301006621994407?journalCode=peca), [arXiv preprint](https://arxiv.org/abs/2101.09376)

This theory is based on computer graphics research on abstracted shading. Here are my favorite papers on it (I'm biased about the third one):

* **D. DeCarlo, A. Finkelstein, S. Rusinkiewicz, A. Santella.
Suggestive Contours for Conveying Shape.
ACM Transactions on Graphics (Proc. SIGGRAPH 2003), Vol. 22, No. 3, pp. 848-855, July 2003.** 
[Project page](https://gfx.cs.princeton.edu/proj/sugcon/)

* **Y. Lee, L. Markosian, S. Lee, J. F. Hughes. 2007. Line drawings via abstracted shading. ACM Trans. Graph. 26, 3 (July 2007).**
[Paper](https://dl.acm.org/doi/10.1145/1276377.1276400)

* **T. Goodwin, I. Vollick, A. Hertzmann.  Isophote Distance: A Shading Approach to Artistic Stroke Thickness. NPAR 2007.**
[Project page](https://www.dgp.toronto.edu/~todd/isophote/)

Also, a significant precursor is the 1985 work by [Pearson and Robinson](https://ieeexplore.ieee.org/abstract/document/1457470).