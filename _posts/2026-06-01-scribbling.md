---
layout: page
title: "Scribbling, abstract art, and visual recognition"
summary: Interesting connections between sketching and human vision
author:  AaronHertzmann
image: "/images/iphone_drawings/sax.jpg"
og:image: "/images/iphone_drawings/sax.jpg"
---

# Scribbling, abstract art, and visual recognition

Sometimes when I sketch quickly, I feel like I'm scribbling some random squiggles, and, yet, recognizable shapes of my subjects emerge:

<center>
<img src="../../../images/ipad_paintings/grandview.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/berkeley.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/pool.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/workshop.jpg" width="240" height="240">
</center>


This experience feels a bit like magic when it works out, like pure fluid intution. And, to me, the drawings are visually interesting because many of the strokes do not correspond to visually-meaningful features, [the way more conventional line drawings do](/2020/09/12/how-to-draw-pictures-contours.html).

This kind of scribbling also shows up in more-recognizable drawings. A lot of drawing a scene is about filling in plausible, sensible details rather than precisely drawing what's actually there.

<center>
<img src="../../../images/ipad_paintings/alley.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/rainyday.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/ragusa.jpg" width="240" height="240">
</center>



Here are a few drawings of dogs; key outlines and features are visible, but a lot of the detail and texture is just scribbling:

<center>
<img src="../../../images/ipad_paintings/rue.jpg" height="240" width="240">
<img src="../../../images/ipad_paintings/lolo.jpg" height="240" width="240">
<img src="../../../images/ipad_paintings/matcha.jpg" height="240" width="240">
<img src="../../../images/ipad_paintings/fozzie.jpg" height="240" width="240">
</center>

Sometimes I like to think of my sketching as "continually scribbling until it doesn't look wrong."

# Statistical recognizability

To me, these kinds of drawings are suggestive of a sort of "statistical visual recognition," by which I mean "recognition from statistics of a single image." These drawings do not necessarily have natural visual features like contours, nor do they seem to fit with the usual demonstrations of Gestalt principles or the visual illusions (e.g., Kanizsa triangle) that illustrate perceptual inference. It's not just scale space; e.g., downsampling the picture doesn't make the object more recognizable, as  like in Impressionism, [hybrid images](https://en.wikipedia.org/wiki/Hybrid_image), or [Arcimboldo paintings](https://en.wikipedia.org/wiki/Giuseppe_Arcimboldo).


Instead, they seem more statistical, and, several abilities of human vision have been described in terms of the statistics of an image, including [texture recognition](https://www.cns.nyu.edu/pub/eero/portilla99-reprint.pdf), [peripheral vision](https://www.annualreviews.org/content/journals/10.1146/annurev-vision-082114-035733), and [rapid scene recognition ("gist")](http://olivalab.mit.edu/Papers/Oliva04.pdf). With some image classification deep networks have shown similar textural recognition properties, such as the adversarial examples in the  ["intriguing properties" paper](https://arxiv.org/abs/1312.6199) and a paper that showed that these networks relied heavily on texture recognition, ignoring shape and other 3D information.


As a model for what's going on here, the work of artist Tom White offers something very suggestive. For example, here's a picture of an electric fan that Tom created in 2018:
<center>
	<figure>
		<img src="../../../images/tom_white_fan.webp" width="480" height="480">
	</figure>
</center>
To create this print, he created an algorithm that optimizes the placement of strokes and blobs, [maximizing the confidence with which a state-of-the-art image classification algorithm (as of 2018) classified the image as "electric fan."](https://medium.com/artists-and-machine-intelligence/perception-engines-8a46bc598d57).

Here are a few more images from that series: each image is optimized to look like a different object class:
<center>
	<figure>
		<img src="../../../images/treachery_of_imagenet.webp" width="467" height="480">
	</figure>
</center>
You can see [more of his work here](https://drib.net/), including abstract pictures [optimized to activate NSFW classifiers](https://medium.com/artists-and-machine-intelligence/perception-engines-8a46bc598d57). Those [examples look abstract to us](https://dribnet.bigcartel.com/product/pitch-dream), but to NSFW filters (as of 2018), they look absolutely smutty. I'm not including them here, just to be safe, because I don't want to this post to be tagged as explicit content.

There are other examples, like Matty Mariansky's [Evolutionary Faces](https://www.aiartonline.com/highlights-2020/matty-mariansky/). I think this also relates to other ideas in different kinds of ambiguous imagery, such as Rob Pepperell's notion of [indeterminate imagery](https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2011.00084/full), which can be [produced by machine learning models too](https://arxiv.org/abs/1910.04639).

# The path to abstraction 

Abstract art seems foreign and obscure to a lot of people. How do you appreciate it?

For me, one gateway to appreciating abstract art has been on a path from realism—what I would now describe in statistical terms. One of my favorite artists is Richard Diebenkorn, and you can see something like a progression or continuum from realism to abstraction in his work:

<center>
<img src="../../../images/arthistory/diebenkorn/diebenkorn-berkeley.jpg">
<a href="https://www.phillipscollection.org/collection/interior-view-ocean"><img src="../../../images/arthistory/diebenkorn/diebenkorn-tea.jpg" width="25%"></a>
<img src="../../../images/arthistory/diebenkorn/diebenkorn2.jpeg" width="25%">
<img src="../../../images/arthistory/diebenkorn/diebenkorn1.jpeg" width="25%">
<img src="../../../images/arthistory/diebenkorn/diebenkorn-ocean-park-73.jpg" width="25%">
</center>

The last one is from Diebenkorn's Ocean Park series, painted when he lived near the beach in Southern California. In the Ocean Park paintings, you can see the general statistics of beach landscapes. There are small shapes near the horizon and large shapes near the bottom, just as there would be in a perspective drawing or photograph with the camera near the horizon.

Many historical Modern artists, and their precursors, who began realistic, but then stripped away some notion in their processes. For example, [Piet Mondrian painted realistic trees, then increasingly abstract trees, ultimately evolving toward the purely abstract style](https://ideelart.com/blogs/magazine/the-evolution-of-style-in-piet-mondrian-artwork) for which he was most famous.  This took him over a decade.

<center>
		<img src="../../../images/arthistory/mondrian/mondrian1.jpg" height="240" width="240">
		<img src="../../../images/arthistory/mondrian/mondrian2.jpg" height="240" width="240">
		<img src="../../../images/arthistory/mondrian/mondrian3.jpg" height="240" width="240">
		<img src="../../../images/arthistory/mondrian/mondrian4.jpg" height="240" width="240">
		<img src="../../../images/arthistory/mondrian/mondrian5.jpg" height="240" width="240">
		<img src="../../../images/arthistory/mondrian/mondrian6.jpg" height="240" width="240">
</center>

I think there is a strong case to be made that the aesthetics of abstraction are tied to the statistics of real experience, including old observations that [image statistics can predict aesthetics](https://www.biorxiv.org/content/10.64898/2026.04.14.718404v1.abstract), and [Jackson Pollock paintings share key statistical properties with real-world imagery](https://www.sciencedirect.com/science/article/pii/S0042698910002129).

I see my own scribblings as a move toward abstraction. In the few situations when [I have experimented with abstract drawing](/2020/11/02/abstract-painting.html), I'm using the skills of realistic drawing (and scribbling), but removing recognizability.

One way this manifests is when sketching on my phone, with my finger, which is naturally quite clumsy:

<center>
<img src="../../../images/iphone_drawings/tube.jpg"  alt="London tube sketch" width="360" height="360">
<img src="../../../images/iphone_drawings/sax.jpg"  alt="Saxophone sketch" width="206" height="360" >
</center>

(The left picture was a drawing I made on my phone while traveling on the London Tube and looking at peoples' shoes.)

Another way is when I try to draw scenes out the window of an airplane (as [mentioned in that previous post](/2020/11/02/abstract-painting.html)): the landscape is continually changing, so it's impossible to capture a "snapshot:" any drawing is just pulling visual elements from what I see and mostly just creating some abstraction. Here are drawings from two plane flights:

<center>
<img src="../../../images/ipad_paintings/abstract/Untitled - July 1, 2023 09.01.31.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - July 1, 2023 09.07.05.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - July 1, 2023 09.09.56.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - July 1, 2023 09.12.29.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - July 1, 2023 10.09.39.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - July 1, 2023 10.37.57.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - June 22, 2024 20.57.10.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - June 22, 2024 21.17.12.jpg" width="240" height="240">
<img src="../../../images/ipad_paintings/abstract/Untitled - June 22, 2024 21.23.24.jpg" width="240" height="240">
</center>

# Directions

Many of these ideas have been explored in the vision science literature in some way, but I think there's more to do here. Specifically, the idea of image recognition as being based on statistical properties, together with the role of statistical descriptions of both realistic (but scribbly) and the hypothesis that abstract art "works" in relation to familiar, real-world scene statistics.