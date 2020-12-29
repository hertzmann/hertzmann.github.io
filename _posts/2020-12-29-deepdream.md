---
layout: page
summary: How dataset choices long ago unexpectedly produced an AI art phenomenon.
author:  AaronHertzmann
image: /images/deepdream/dogception.jpg
---


# Why DeepDream Dreams of Doggies


The [DeepDream algorithm](https://ai.googleblog.com/2015/06/inceptionism-going-deeper-into-neural.html) creates hallucinatory imagery, fantasizing elements of architecture and animals from input images. The algorithm [made a big Internet splash when it came out in 2015](https://knowyourmeme.com/memes/subcultures/google-deepdream).  An algorithm meant to provide a relatively ordinary visualization task produced [wild imagery that some people compared to LSD trips](https://www.theatlantic.com/technology/archive/2015/09/robots-hallucinate-dream/403498/) and perceived as ["creativity in the mind of the machine"](https://slate.com/technology/2015/07/google-deepdream-its-dazzling-creepy-and-tells-us-a-lot-about-the-future-of-a-i.html).

DeepDream was, arguably, a novelty. However, it was one of a few algorithms that launched new interest in AI algorithms for art, around which a new community has grown, and continues to grow. 

Here's one of the first images from the original description of DeepDream:

<center>
<figure>
  <img src="../../../images/deepdream/sky.png" alt="DeepDream sky"/>
</figure>
</center>

and some of the structures they found:

<center>
<figure>
  <img src="../../../images/deepdream/dd-animals.jpg" alt="Admiral Dog, Pig-Snail, etc."/>
</figure>
</center>

These structures resemble creatures, often some sort of dogs. And, the more images people produced using higher-level network layers, [the more dogs appeared](https://twitter.com/search?q=deepdream%20dog).

Why dogs?

It turns out that DeepDream's obsession with dogs isn't because they're cute; it's an accidental by-product of history. Specifically, [as pointed out by an ImageNet coauthor](https://news.ycombinator.com/item?id=9818077), it's because there are a lot of dogs in the dataset. It's worth understanding why.
There's new attention recently to analyzing the [contents](http://www.salavon.com/work/little-infinity-v-mfah/) and [structures](https://www.excavating.ai) of datasets. DeepDream doggies present a small-but-interesting case study in the unexpected effects of a seemingly-minor technical choice made long ago.  

Maybe our current era of AI art wouldn't have taken off in the same way, were  it not for this one little choice made years ago.


# Toward Fine-Grained Classification

The [ImageNet dataset was developed over several years in Fei-Fei Li's lab](http://image-net.org/about-publication), with the aim of creating the first very large dataset for computer vision. In the initial publication in 2009, it comprised a large collection of images scraped from the web and loosely labeled by human annotators. However, these crowdworker annotations were not very good, or very meaningful. 

In order to get better annotations, the researchers, led by Jia Deng, devised [a more rigorous annotation methodology](http://ai.stanford.edu/~olga/papers/chi2014-MultiLabel.pdf). But this methodology was more expensive and time-consuming, so [they had to narrow it down to a _challenge_ subset](https://arxiv.org/abs/1409.0575) of 1000 categories.  What should those categories be?

These 1000 categories were chosen to test different aspects of a vision system's performance. On one hand, most of the categories were aimed at testing coarse image classifications, e.g., being able to distinguish lobsters from teakettles.
But vision isn't just coarse image categorization. They also wanted to test fine-grained categorization within some class of objects. What should the fine-grained categories be?  Previous fine-grained datasets had been based on object categories like [birds](http://www.vision.caltech.edu/visipedia/CUB-200.html) and [clothing style](https://vision.cornell.edu/se3/wp-content/uploads/2014/09/iwmv2013_style_detection.pdf). 

For whatever reason, [they chose dogs](http://vision.stanford.edu/aditya86/ImageNetDogs/main.html). Starting with the 2012 version of the challenge dataset, they included many different dog breeds, since distinguishing a miniature schnauzer from a dalmation is a very different problem from distinguishing a lobster from a teakettle.

As a result, [**dogs represent a whopping 12% of the challenge dataset**](http://image-net.org/challenges/LSVRC/2014/browse-synsets). The challenge, known as **ILSVRC2014**, was won by a network called [Inception](https://arxiv.org/abs/1409.4842). And then other researchers began to work on visualizing how Inception works.

<center>
<figure>
  <img src="../../../images/deepdream/imagenet_figure.jpg" alt="ImageNet dog category figure"/>
  <figcaption align="center"><i>An image from <a href="https://arxiv.org/abs/1409.0575">the ImageNet paper</a> illustrating fine-grained categories, as compared to PASCAL, a previous dataset.</i>
 </figcaption>
</figure>
</center>



# Cry "DeepDream," and Let Slip The Dogs of ImageNet

DeepDream, [created by Mordvintsev et al., began as a visualization technique](https://ai.googleblog.com/2015/06/inceptionism-going-deeper-into-neural.html), creating images likely to "excite" intermediate neurons. That is, it seeks to answer the question: what kind of images "excite" the Inception network the most?

The answer is, to a large extent, images with dogs. If, over your entire life, you saw dogs 12% of the time when you're eyes were open, you'd have dogs on the brain too. [As pointed out by one of the ILSVRC coauthors](https://news.ycombinator.com/item?id=9818077), **DeepDream makes dogs because it's seen them so often**.

DeepDream also makes creatures, buildings, and vehicles. And, indeed, looking through [the categories in ILSVRC2014](http://image-net.org/challenges/LSVRC/2014/browse-synsets), many of the categories are creatures, buildings, and vehicles. There are also numerous household object categories, but these don't appear as much in DeepDream, perhaps because they are more visually dissimilar to each other. That is, all birds have eyes and beaks, but "soccer ball," "saxophone," and "umbrella" don't have much in common visually.  Notably, there  very few people in DeepDream; [ILSVRC2014 only includes three person categories](http://image-net.org/update-sep-17-2019) (and one of them is "scuba diver"), though people may appear in other images in the dataset.

Although generative art and AI art have been around for nearly six decades,  DeepDream helped popularize it for a new generation. [Artists began to explore DeepDream](http://www.miketyka.com/?s=deepdream), a first step toward "AI artist" being a category in itself today.  


<center>
<figure>
  <img src="../../../images/deepdream/gray_area_show.jpg" alt="DeepDream art show"/>
  <figcaption align="center"><i>An art exhibition around DeepDream and Neural Style Transfer. Gray Area Gallery, San Francisco, 2016. (Thanks to Leon Gatys for letting me have one of his free tickets to the show.)</i></figcaption>
</figure>
</center>

[DeepDream wasn't the first algorithm to create this kind of feature map visualization](https://arxiv.org/abs/1312.6034), but it was the first to become Internet famous.  Would DeepDream have been so popular without the dogs and other creatures? 

Here are some later images, computed using DeepDream with networks trained on other categories (places and cars), [taken from this website](https://www.sprawledoctopus.com/deepdream/datasets):

<center>
<figure>
  <img src="../../../images/deepdream/dd_others.jpg" alt="DeepDream on different datasets"/>
</figure>
</center>

[In the conventional DeepDream, evocative doggies appear](https://www.sprawledoctopus.com/deepdream/datasets/img/example-google1.jpg), whereas [the structures in the other images, while interesting, don't have the same power](https://www.sprawledoctopus.com/deepdream/datasets/img/example-place1.jpg).  

If, years earlier, the ILSVRC creators had instead focused on fine-grained categorization of cars or places, and DeepDream only made mutant cars or buildings, then perhaps it would not have excited imaginations quite the way it did, or helped launch an AI art movement the way that it did.


*Thanks to Alex Berg for reading an early draft of this.*
