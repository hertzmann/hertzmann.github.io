# Why Edge Detection Doesn't Explain Line Drawing


Why do line drawings work? Why is it that we can immediately recognize objects in line drawings, even though they are not a phenomenon from our natural world. Numerous studies show that people who have never seen a line drawing before can understand a line drawing; line drawing is not something you have to learn to understand. 
Vision 

Vision researchers generally believe that this question is answered by what I will call the **Lines-As-Edges hypothesis**. Roughly speaking, it says that line features activate edge receptors in the human visual system, and it is well known that human vision is much more sensitive to gradients than to absolute intensities. From what I can tell, this belief is widely shared; many people bring it up whenever I discuss this problem with them, as did [many commenters on a recent Twitter thread](https://twitter.com/hardmaru/status/1250979159779635200?s=20).  A generalization of this is that lines correspond to some internal representation, such as neurons that fire on object contours, which I'll call **Line-As-Internal-Representation** and also discuss here.

The purpose of this blog post is to explain why I think you should be skeptical of the **Lines-As-Edges hypothesis**. Most vision researchers and tweeters state some version of the hypothesis with uncritical certainty, as it the problem is solved, and I seem to have a hard time convincing them to be at all skeptical of it.  It has the feeling of unquestioned, received wisdom: everyone knows that this is true, and no one has thought any further than that.

I don't claim that **Lines-As-Edges** is necessarily false, but I do argue that it is unsatisfyingly incomplete, and that further understanding is required. In a [recent paper](https://journals.sagepub.com/doi/abs/10.1177/0301006620908207?journalCode=peca) [(preprint version)](https://arxiv.org/abs/2002.06260), I proposed a totally different explanation for line drawing. While my explanation is also incomplete, I think it provides some potential benefits. Morevoer, people shouldn't be so quick to consider line drawing as completely explained by **Lines-As-Edges**.  


What is the Hypothesis?
------------

In order to argue for or against the hypothesis, we need a clear statement of what it actually says. Yet, for being so widely accepted, it's very hard to find such a statement.  The only real statement of *Lines-As-Edges* that I've found is by [Sayim and Cavanagh (2011)](https://www.frontiersin.org/articles/10.3389/fnhum.2011.00118/full), but the idea has certainly been "in the air" for decades.  I'm sure I heard it many years ago, and I don't remember where.

At a high-level, the idea arises from two observations. First, since the pioneering experiments of Hubel and Wiesel (1962), we know that the visual cortex includes cells that are responsive the edge patterns. In short, one of the first thing that happens to the signal from our retinas is edge detection.  Second, if you run an edge detector on a real image, and threshold the responses, then you often get something that looks like a line drawing.

Here is an example of the Difference-of-Gaussians edge detector, from the [XDoG paper](https://www.kyprianidis.com/p/cag2012/):

![Difference-of-Gaussian filter](../../../images/DoG.jpg)

The most basic statement of the hypothesis is then something like: the lines in a line drawing are drawn at point corresponding to image edges, where an edge receptor would fire. These lines activate the same edge receptor cells. Hence the line drawing produces a cortical response that is very similar to that of an original image.

As compelling as this idea is, only the one paper (that I've found) by Sayim and Cavanagh attempts to state it clearly, and even they point out big holes in the idea.  No one else (that I've found) has attempt to formulate this theory. Once you do try to formulate it as a theory, big problems arise.  (Some of these problems overlap in scope.)  

In a sense, the most basic problem with the hypothesis is that no one has really explicitly stated what it is in much detail.


Problem #1: What about all the other features?
------------

The most basic statement of the problem with Lines-As-Edges is that the human visual system isn't just an edge detector. You can see colors, you can see absolute intensities. You can tell the difference between a thin black line and an object silhouette; we have both kinds of receptors in the primary visual cortex, as well as others.  Line drawings are, indeed, vastly different than natural images in how they activate many visual features that we are immensely sensitive to.  Yet Lines-As-Edge supposes that the vision system discards all of this information present in an image, for just this one special case. Why?

Discarding some features and not others seems arbitrary. Surely we could discard some other random collection of features and get other plausible image interpretations out of them.

I've never heard a plausible answer to this question, or even seen a concrete attempt to answer it.  


Problem #2: Line drawings are still not natural images
------------

To some extent, Lines-As-Edges does not answer the original question at all. A line drawing does not look like the sorts of things we see in the natural world at all. We can easily tell the difference; we are not blind to all of the non-gradient information. The theory doesn't answer the question of _why_ the human vision system should have such a response to an drawing that is so obviously different from a natural image, rather than just seeing it as marks on a page, screen, or wall. From an evolutionary standpoint, it would seem counterproductive for the vision system to hallucinate a second image on top of the page or wall that, seemingly, is so utterly outside the space of natural images. Making a wrong detection in this case could imply that more wrong detections in more life-or-death situations.  


Problem #3: We can't see internal representations
------------

A slightly different statement of the hypothesis is what I'll call **Lines-As-Internal-Representations**. One statement of this theory is that line drawings work because we have neurons that represent image edges, and line drawings project to these representations.  A more general statement is that we have neurons that activate for object contours and similar, and that line drawings directly activate these neurons.

I don't understand this claim at all. You can't just show some visualization of some arbitrary neuronal activation to the brain and expect that those neurons will fire.

Suppose you have an algorithm that computes `y=f(x)`, and the computation involves an intermediate variable: `w=g(x); y=h(w)` so that `f(x)=h(g(x))`. You cannot expect to get the same result if you run `w=g(x); y=f(w)`. The types might not even match.  In terms of neural networks, this theory seems to be proposing that you can take filter output `i` from network layer `j` and directly feed it as input to the network. How would this even work?


Problem #4: What is the benefit?
------------

To really understand vision, we have to reason about more than just the visual cortex. If human vision was just edge detection, then we would have already figured out how vision works a long time ago.  Understanding vision by looking only at neurons is like trying to understand how a computer program works by looking only at the compiled machine instructions and not thinking about what the program is for.

The human vision system is extraordinarily robust at what it does: help us navigate and survive the world by providing us high-quality inferences about what we see. This process is extremely robust to all sorts of misleading and noisy sources of information.  Any explanation for how it can be fooled into inaccurate perception requires a compelling explanation in terms of the _goals_ of the vision system. For example, [Adelson's checkerboard illusion](https://en.wikipedia.org/wiki/Checker_shadow_illusion) indicates that the visual system is much more interested in inferring actual reflectances rather than incoming irradiance, and that giving our cognition access to retinal measurements is important to our survival (in the evolutionary sense).  Most visual illusions exploit inductive biases of the vision system that are normally useful, but create unexpected outcomes in cases that didn't matter that much to our Pleistocene ancestors. 

Lines-as-edges posits a massive "failure" of visual inference&emdash;hallucinating shape where there is none&emdash;without providing any corresponding beneficial inductive bias.  We don't actually believe the shape is there due to (the dichotomous nature of images)[https://www.frontiersin.org/articles/10.3389/fnhum.2015.00295/full], but the inference of shape is still, in some, sense, entirely erroneous under this hypothesis.



Problem #5: Edge detection is not a line drawing algorithm
------------

As an aside, there is another problem with Lines-As-Edges, which most commenters do not seem to be aware of. I think it can be fixed, as described below.

Lines-As-Edges starts from the observation that edge detection produces line drawings. But it often doesn't.  Here are two examples from Sayim and Cavanagh:

![Lines vs. Edges](../../../images/sayim.jpg)

That said, I think that Lines-As-Edges could be modified to account this, combining ideas from [Judd et al. (2007)](http://people.csail.mit.edu/tjudd/apparentridges.html) and [my paper](https://journals.sagepub.com/doi/abs/10.1177/0301006620908207?journalCode=peca).  The modified LAE hypothesis would be: the visual system interprets line drawings as if they were edge images of a matte white object under headlight illumination, or averaged over a range of similar illumination. To my knowledge, this modified hypothesis is novel; except that Judd et al. make very similar assertions that come extremely close to this.

However, this modification does not fix the other problems listed above.


Problem #6: Visual art isn't just line drawings
-------------

Suppose we add color to a line drawing:

![Watercolor apple](../../../images/apple-watercolor2.jpg)

Now you get a sense of the color of the object, and not just its outlines.  How would one generalize Lines-As-Edges to account for these different types of depiction? Now the visual system is no longer ignoring everything but certain gradients; it's paying attention to some colors (and not others).  Or suppose we add hatching:

![Hatching apple](../../../images/apple-sketchy2.jpg)

How does Lines-As-Edges now explain our perception of this style?

Artists depict objects in a seemingly-infinite combination of outlines, colors, hatching, stippling, painting, and so much else. To account for this, the Lines-As-Edge hypothesis would need to argue that somehow the visual system recognizes each style and identifies which features to ignore and which to keep.  Again, this may be true in some, but it should be clear that Lines-As-Edges is far from being the end of the story.

Alternatively, it could be that untrained observers cannot understand these drawings; I am not aware of any studies on this topic, but I think it unlikely, since studies have shown that untrained observers can understand line drawings and they can understand photographs.



Alternatives
------------

I believe (my hypothesis)[https://journals.sagepub.com/doi/abs/10.1177/0301006620908207?journalCode=peca] proposes an alternative solution that does not have the problems listed above. This hypothesis is compatible with Lines-As-Edges, while answering many of the questions above.  The hypothesis is itself quite incomplete, but I think it provides a much more insight and a promising path toward answering the line drawing question.