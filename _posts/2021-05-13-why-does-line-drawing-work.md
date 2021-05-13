# Why Does Line Drawing Work? A Realism Hypothesis

This page summarizes my new hypothesis about why line drawings work, which was published in a vision science journal in 2020 and 2021. You can also watch [a presentation of this work on YouTube](https://www.youtube.com/watch?v=FxrwJFjGyP4).  <a href="#citations"><b>Paper links.</b></a>

**We begin with a mystery.** We have eyes and vision in order to help us navigate and survive in the real world. Evolution gives us abilities to quickly and accurately understand images of the real world. If you see a picture of the forest at night in the fog, you can immediately tell what it is and recognize objects in the scene. Being able to accurately, quickly, and continually understand the world around us helps us find food, avoid danger, and live together with other people.  Mistakes in vision–like hallucinating something that isn't there–can lead to misunderstandings, accidents, or even death.

It's not too surprising that we can understand photographs, since they look a lot like the real world. But what about line drawings? These look nothing like the real world. We don't see black pen outlines walking around on white backgrounds.  Yet, we can understand drawings just as easily as we can understand photographs. Why would this be?

<center>
![Drawing of a cartoon fox](/images/howtodraw/fox.jpg)
</center>


If you can understand real images, you can understand basic line drawings
=====

[One influential philosophical theory](https://en.wikipedia.org/wiki/Languages_of_Art) holds that all artist styles are learned from our cultures and upbringings.  We learn to understand line drawings when we are children, in the same way that we learn to understand written language. All artistic styles are products of our cultures.

Yet, line drawings exist throughout many different historical cultures, even preceding civilization. Cave paintings made by our prehistoric ancestors using outline drawing and are easily recognizable to us today. Moreover, [numerous studies with members of tribal societies](https://journals.sagepub.com/doi/10.1068/p040391) show that **someone who has never seen a picture before can understand what's in a line drawing.**

I wondered if perhaps understanding line drawing is a consequence of real-world vision. Specifically, I hypothesize that **if we could train a computer vision algorithm to understand 3D shape in real-world imagery just as well as humans, then that algorithm would also be able to understand shape in line drawings.**  While our current computer vision algorithms aren't nearly as good as humans, I tried this out with [a method that was state-of-the-art at the time](https://arxiv.org/abs/1907.01341v1). This deep neural network predicts relative depth for each pixel in a photograph:

![Depth estimation results on photos](/images/howtodraw/midas-real.jpg)

Importantly, this model was solely trained on photographs, not on drawings. And, when I tried it on some line drawings, I got similar results!

![Depth estimation results on drawings](/images/howtodraw/midas-drawing.jpg)

This shows that perception of line drawing must be somehow a consequence of real-world perception. But what is the connection?

(Many vision researchers have hypothesized that line drawing perception is a consequence of edge receptors in the early stages of the human vision system, but [I think this is implausible for many reasons.](/2020/04/19/lines-as-edges.html))


Line drawing as Abstracted Shading
=====

It turns out that there's a way to create line drawings that roughly looks like it could be a real-world situation.

Set up a 3D object in front of you. Paint it white. Turn off all the light sources, except for a headlamp that you wear on your forehead. If the object is a model of a cow, it may look like this:

![Diffuse rendering of a cow](/images/howtodraw/cow_diffuse.png)

If we draw a picture of this image with a black pen on white paper, the simplest thing to do is to draw lines through the darkest regions. And that picture might look like this:

![Line rendering of a cow](/images/howtodraw/cow_thick.jpg)

We can see that _the drawing is, approximately, a plausible real-world image._ That is, it's not something that we're likely to see around us. But we are able to understand realistic photos of things we've never seen before-even when the image is corrupted with fog or rain or image noise-and this rendering setup shows how a realistic setup can approximately produce line drawings. [This model of line drawing originated in computer graphics research.](/2020/09/13/how-to-draw-pictures-suggestive-contours.html)

This setup works with various different settings of materials and lighting; here are two other possible examples. In each case, the lines are being determined by [a valley-detector algorithm]() (in OpenCV):



| I hypothesize that, for a person who has never seen a picture before, **the human visual system interprets a line drawing as if it were a realistic image, with a lighting and material setup similar to those above.** |


![Valleys of a 3D model with glossier materials](/images/howtodraw/david_valleys.jpg)
![Valleys of a photograph](/images/howtodraw/photo_valleys.jpg)

This hypothesis doesn't say anything about how the vision system actually works. It says that, whatever the vision system is doing, it does basically the same thing for a line drawing as it does for the corresponding realistic 3D rendering.



Future directions
====

This hypothesis could be tested by fMRI experiments with human subjects. I predict that the neural responses to a line drawing will be very similar to those of corresponding 3D renderings. There are some previous neuroscience studies that have been performed comparing neural responses of line drawings to photographs; these methodologies could be used to test my predictions. This could also be used to assess what kinds of lighting and material setups best match line drawings.

This theory focuses solely on a very basic line drawing style, treating it as a form of **abstracted shading**. In the paper, I discuss how several other types of line drawings-such as white-on-black drawing and hatching-can also be understood as abstracted shading. But the range of visual artistic styles we can understand is vast; we seem to have the ability to visually separate style from content. How do we do this?

<a name="citations">
Citations
=====

These ideas were first described in the following paper:

* **Hertzmann A. Why Do Line Drawings Work? A Realism Hypothesis. _Perception_. 2020. 49(4):439-451.** [Official paper link](https://journals.sagepub.com/doi/abs/10.1177/0301006620908207?journalCode=peca), [arXiv preprint](https://arxiv.org/abs/2002.06260)

The second paper expands on how this hypothesis relates to theories based on edge detection. It is meant to be self-contained, and may be easier to read:

* **Hertzmann A. The Role of Edges in Line Drawing Perception. _Perception_. 2021. 50(3):266-275.** [Official paper link](https://journals.sagepub.com/doi/abs/10.1177/0301006621994407?journalCode=peca), [arXiv preprint](https://arxiv.org/abs/2101.09376)