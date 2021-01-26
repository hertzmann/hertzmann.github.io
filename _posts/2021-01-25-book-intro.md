---
layout: page
title: "Understanding Visual Art as Computation: A Hypothetical Book Introduction"
summary: An outline/summary of my research around understanding art
author:  AaronHertzmann
image: /images/wica/bradford_viewers.jpg
redirect_from:
  - /2021/01/25/2021-01-25-book-intro.html
---

# Understanding Visual Art as Computation: A Hypothetical Book Introduction

*This blog post is an attempt to outline some of my main ideas and research around understanding visual art, in the form of a hypothetical introduction for a hypothetical book. This book would be written for a general audience (e.g., no equations, though with extensive references to the technical literature).  It's a cross between a book proposal and a "brain dump." Links to things already partly written now are in [the outline below](#outline).*

----


**This book presents a vision for how computational models help us understand visual art. Better understanding of art leads to better appreciation and enjoyment of it; it provides new ways to teach art. Computational models lead to many insights that we could not find any other way. And better understanding leads to new technologies that create new tools for arists and enable new kinds of art and artistic expression.**

In my own studio art studies in college, I frequently struggled to understand the feedback from my teachers. For example, in one class we did open-air watercolor painting. On the first day, I brought back a street scene I was proud of. [The professor criticized all the details I drew, asking "why did you draw that street sign?"](https://aaronhertzmann.com/2020/09/15/painting-in-karies.html) I said I drew it because it was there, and, to me, drawing a picture of the scene meant capturing everything I saw. I didn't understand what else it could be. And my picture was a bit of a mess, too obsessed with fine details at the expense of the overall composition.

As I continued in these studies, I got better intutions for how to paint, but I could never articulate what I was doing or why.  Likewise, my art professors used a language that was indirect and vague; the "rules" for one artwork—why the artworks "succeeded" or "failed"—seemed different from the "rules" for the next one.  In short, art instruction was primarily about training intuitions and skills based on high-level guidance. Our teachers acted more like travel agents than tour guides: they could help you figure out where to visit, but they did not have maps or street directions.  This isn't our teachers' fault. Our languages for talking about art are quite limited; some would say necessarily so, like in the famous Laurie Anderson quote: "talking about art is like dancing about architecture."  But we still see value in art criticism, discussion, and teaching.  This book presents ways that we can make this language richer and more useful for understanding and communicating about art.


Non-photorealistic rendering
===

When I entered graduate school in computer science, I discovered a subfield of computer graphics called non-photorealistic rendering, which aimed to create algorithms to simulate painting, drawing, and other conventional artistic styles. Pioneers in this field had developed algorithms that could take a photograph and turn it into a painting, or a 3D model and turn it into a pen-and-ink-style line drawing.  Here was a place where I could try to figure out how to turn my own artistic intuitions into algorithms. I started developing a painting algorithm that began by creating a rough sketch of a painting, and then refining the fine details, similar to how I used to paint. Each time I ran the algorithm, I got a new painting. A digital painting, in software, composed of virtual brush strokes, but a painting nonetheless.

In a sense, I was building a theory for how a painter works. This theory is very limited—it was very stylistically limited and it doesn't reproduce how any real painter works. But like any scientific theory, it was a model a very tiny little piece of reality. It is a small stepping stone in the development of scientific models, and one that may be built upon or discarded as models are improved.

Over several decades of research, the theory and algorithms of non-photorealistic rendering advanced by researchers in the field. Most of us thought we were developing computer graphics algorithms, to provide better tools for artists. But I believe we were also building scientific theories along the way.

Today, this body of knowledge forms **a generative description of visual representational art**. That is, we can describe some of the ways that representational artists turn 3D understanding into drawings and paintings. This is the main subject of Chapter 2. 

The generative theory doesn't explain *why* art works. Nor does it attempt to say that one kind of art is better than another. It just provides a description of many different styles of art.

However, the generative theory can help understand the perception of art. For example, one long-standing question in psychology is why it is that we can understand line drawings, even though line drawings do not exist in the natural world. Many psychologists and philosophers have wondered this over the decades, without a satisfactory answer. 
One of the main achievements of non-photorealistic rendering is a theory for line drawing which, as I will describe, is key to answering the perception question as well.

Although computing plays a central role in my explanations, this is not to say that computer science is somehow better at understanding art than are other areas of science. Perceptual psychology, neuroscience, machine learning, computer vision, and the  philosophy of art all play crucial roles. The book aims to be a synthesis of ideas from different disciplines, rather than some sort of argument for the supremacy of computing.


Art is construction, not perception
===

We often talk about artworks as if they let us "see through the artist's eyes."  This is a mistake: an artwork is a construction, where an artist has made choices to arrange paint or pencil strokes, or even made choices about where to aim their camera. Even though Gombrich's famous book _Art and Illusion_ made this main point in the 1960s, we still see people making this same mistake over and over again. I have seen this mistake when people respond to my own artwork; this is a mistake made by those who explain Van Gogh's creativity as a product of visual hallucinations, and so on.

Art is the product of choices made by the artist in order to achieve an experience in the viewer; it is not a recording of experience: this the theme of the first chapter.  While this is not a point that is specifically about computing, it is important to understand when understanding how artists work. And it's something that manifests again and again in our technology. 

Even in photography, the artist and the camera make important choices in how to depict a scene. The implicit belief that photography is purely objective is a dangerous tool for misinformation and propaganda. As we will see, simple engineering decisions in the design of cameras can sometimes have important political and social implications.

An artist may attempt to portray their perception, just as I attempted to portray my perception in my painting classes. But all attempts to portray visual experiences are incomplete. No artist can perfectly record their experiences. The best artists create vivid new experiences—whether aesthetic, emotional, and/or intellectual—and some excel at suggesting a sliver of their own experiences along the way.


Neuroscience and neural networks
===

About a decade ago, progress in non-photorealistic rendering research slowed to a crawl. Perhaps the field was too focused solely on computer science ways to understand art. Meanwhile, neuroscience and machine learning have produced new ways to understand and create art, and it is often unappreciated the ways in which these fields are intertwined; this is the main topic of Chapter 3.

In the last 1950s, a set of biological experiments discovered that the first part of neural visual processing includes edge detectors. As neuroscientists better understood the biology of how our brains process images, they created better and better computational models of the brain. These models eventually led to modern artificial neural networks, which have powered our modern AI revolution. In turn, these computational models have led to better theory and understanding of how the brain works. One of the main arguments of this book is that the same synergy of biology and computational models should inform our understanding of art.

Along the way, neuroscientists and vision researchers attempted to build neural models of texture processing.  These models led to generative models of texture.  Then, myself and others realized that these texture models could be used to "transfer" artistic styles, for example, to automatically create a photograph look like a Van Gogh painting. Using modern neural networks made these techniques particularly effective, as in the popular Neural Style Transfer algorithm. However, as one of the members of my PhD committee pointed out to me, these methods are all "just texture."  A developing line of research aims to combine learned and procedural models, to gain richer models of style while maintaining the benefits of machine learning.


Neural network art
===

Meanwhile, generative neural networks and image translation networks have been exploited by artists to create new styles of visual art.  Most significantly, Generative Adversarial Networks have been exploited by artists in many ways, along with less-prominent technologies but on neural networks, like DeepDream and image translation. These methods, briefly surveyed in Chapter 3, reflect the main themes of this book: they illustrate how new scientific understanding and technology has led to new kinds of art.
 
Ambiguity and abstraction
===

The first few chapters  are focused on fairly conventional and classical styles of art. Indeed, I came away from my own art education having little conceptual framework for how to understand or create abstract art. I knew the major artists and movements, and some of the political and cultural forces behind them, but I had no idea how to think about how they worked aesthetically. And I certainly had no idea how to make it myself; my own attempts at abstraction always looked like empty doodles. For me, the notion of perceptual ambiguity has changed that.

Almost everything we see in the world has some sort of ambiguity.  Imagine looking down a dimly lit street at night, seeing what looks like the silhouette of a man walking in the distance. Is it a man, or just a hedge, or a lampost? Is he walking toward you or away? Is it someone you know or a stranger?  

Though we are rarely conscious of it, ambiguities like these play an enormous role in our perception. Moreover, this example shows how ambiguity can be emotionally loaded: depending on the context, and your experience, ambiguity can make you curious, eager to learn more and resolve the ambigiuty, or it can make you unsettled and afraid.

Artists exploit and mine ambiguity. 
All art exhibits some sort of ambiguity, even a *trompe l'oeil* appears simultaneously to be a real object or just a painting of one. Moreover, ambiguity is, arguably, *the dominant yet unsung theme of modern and contemporary art;* learning to appreciate modern art requires cultivating an appreciation for ambiguity (as well as cultivating other kinds of literacy).

Chapter 4 explores how we can understand art through the twin lenses of ambiguity and uncertainty, and a principle of decisionmaking called Bayesian reasoning that originated in probaility theory, was developed in AI, and can explain many neuroscience phenomena. I believe this reasoning provides a useful way to think about and analyze art as well.


Computers are not artists
===

Any attempt to understand the science of art seemingly invariably leads to objections: "are you trying to make artists obsolete?" "you can't understand something so mysterious and personal as art." These objection do not seem to be rooted in any understanding of the technology, but rather in an almost religious belief in art as special force apart from human biology or psychology. Chapter 5 attempts to provide a more informed understanding of how the development of technology and science has affected artistic tools. In short,  automation in artistic tools  has always created new possibilities for artists, and expanded our understanding of art.

Could this ever change? Inspired by evolutionary theories of art, I argue that, even though "automatic artists" have been seemingly around the corner for the past several decades, it's unlikely that technology will ever "make artists obsolete."

The idea that, in the forseeable future, computers will be truly intelligent or treated like artists is a product of hype, not reality. This hype can even be dangerous for society, when biased algorithms are treated as if they are objective and rational, and artists who present their software as intelligent add to this hype.


Ways to understand and appreciate art
===

There are many ways to understand and appreciate art, including cultural, political, historical, psychological, and so on. None of what I'm writing here is meant to diminish the importance of these ways of understanding.  For example, culture, history, and politics are crucial to understanding art—perhaps they are the most important factors of all—I just don't have that much new to say about these things.  

I do believe these ideas can be useful to different kinds of people. Some of the ideas here would have helped me immensely when I was first studying art. I have already made a case for how psychologists and neuroscientists attempting to understand art would benefit from these ideas.

But even if you're not involved in making or studying art, but only in enjoying and appreciating it, I think these insights can be useful. I have always found that better understanding of art led to a better appreciation for it. For example, even though I don't make movies, understanding the three-act structure of most filmmaking helps me understand and talk about movies better than before.  There are certain kinds of problems in filmmaking that may leave you vaguely feeling unsatisfied; understanding the three-act structure and character arc gives you a language for understanding and describing those flaws or appreciating them when done well.  

Likewise, the concept of visual indeterminacy has vastly helped me  appreciate modern and contemporary art, and it has also helped me create abstract art.

But, most important, advancing this understanding advances art.  Historically, many of the most cutting-edge artists did not work in a vacuum; they have and do work in creative communities of artists and critics, and their artwork was often inspired by the critical analysis around them in a virtuous cycle. Understanding the latest developments in technology will help inform the next generation of art from technology. And, equally importantly, it will inspire new artistic tools that inspire new kinds of art.





----

<a name="outline">
# Chapters / Themes

1. **Art is construction, not perception**
	* Big questions:
		* How do generative models and perception relate?  
		* How do we make art? How do we perceive it?
	* [My own experience with the artistic process](/2020/10/05/art-is-a-process.html)
	* Visual art is about creating visual and aesthetic experiences
		* It is not a mirror or snapshot of reality.
		* Photography, persuasion, propaganda. Photography can be an objective measurement but not in the way we think.
		* Tone and color: perception and reproduction. Ecological Valence Theory.
		* Projection systems: there is no "correct" projection
		* Subject, composition, cropping, etc. 
	* Art as optimization
		* [Stroke-based optimization](https://www.dgp.toronto.edu/~hertzman/sbr02/)
		* Reinforcement learning
		* Open-ended exploration

2. **Procedural models of artistic style**
	* [John Willats](https://www.amazon.com/Art-Representation-Principles-Analysis-Pictures/dp/0691087377)
	* 3D Non-photorealistic rendering
		* [Line drawing](/2020/09/13/how-to-draw-pictures-suggestive-contours.html)
		* [Shading and style](https://aaronhertzmann.com/2020/09/14/how-to-draw-pictures-style.html)
	* [Where do people draw lines](https://gfx.cs.princeton.edu/pubs/Cole_2008_WDP/)
	* [Why does line drawing work](https://arxiv.org/abs/2002.06260)
	* Shape: exaggeration and deformation
		* 3D caricature: Susan Brennan, Volker-Blanz
		* Part-wise models, childrens' drawings, etc.

3. **Neural networks and neuroscience**
	* Some history of vision neuroscience and neural networks, AI. What is AI?
	* Texture synthesis
	* [Example-based stylization](https://research.adobe.com/news/image-stylization-history-and-future-part-2/)
		* Image Analogies, Neural Style Transfer, pix2pix, CycleGAN, SPADE
		* These are all "just" texture models
		* Portrait stylization
	* Generative networks
		* GANs
		* DALL-E
	* Future potential

4. **Ambiguity and abstraction**
	* Ambiguity in art, Modern Art, Picasso.
		* Visual appreciation of modern art requires appreciating ambiguity
		* Visual vs. conceptual
	* Value of Information as a biological principle
	* [Types of ambiguity](http://experimental-psychology.de/ccc/docs/pubs/MuthCarbon2016a.pdf)
		* The Aha moment
		* Bistability
		* Dichotomies, e.g., Arcimboldo, Tom White
	* [Neuroscience and predictive coding](https://journals.sagepub.com/doi/10.1068/i0466aap)
	* Visual indeterminacy
		* [Turner, Gerhard Richter, Pepperell](https://www.frontiersin.org/articles/10.3389/fnhum.2011.00084/full)
		* [GANs](https://arxiv.org/abs/1910.04639)
		* [Perceptual studies](http://cybertron.cg.tu-berlin.de/xiwang/tap-project-page/)
	* [Learning to paint abstractly](/2020/11/02/abstract-painting.html)
	* Could we author ambiguity?

5. **[Can computers be artists?](http://www.mdpi.com/2076-0752/7/2/18)**
	* History of artistic technology
		* Watercolor, paints in tubes
		* Photography as artistic machine, from Daguerre to Stieglitz
		* Frieder Nake era
		* Procedural artists (Harold Cohen, Karl Sims)
		* Computer animation (Pixar)
		* Media arts world (e.g., Processing)
		* Current neural network revival (DeepDream, GANs, etc.). Twitter+GitHub.
	* Computers do not create art
	* Could computers be artists in the future?
		* [Definitions of art](/2020/05/19/wiwia.html)
		* [Evolutionary theory and art](https://www.bloomsbury.com/us/the-art-instinct-9781608190553/)
		* Art as social activity