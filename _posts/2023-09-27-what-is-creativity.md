---
layout: page
title: What is Creativity, and Can Computers Be Creative?
author:  AaronHertzmann
image: "/images/wica/bradford_viewers.jpg"
og:image: "/images/wica/bradford_viewers.jpg"
---

# What is Creativity? Can Computers Be Creative?


Whether computers can be creative or not comes up a lot these days. Sometimes it's assumed they can be, like in some of the court cases. I get the question a lot when [I give talks on computers as artists](https://www.youtube.com/watch?v=ZOv3GizIUE0) (and why I don't think they can be considered artists). 

In this post, I'll describe how I now think about creativity. I've written a lot about it over the past few years, [from some initial questions about computational creativity](/2021/04/19/questons-for-computational-creativity.html), to [reflecting on my own progress in painting and drawing](/2020/10/05/art-is-a-process.html), and [comparing that to using DALL-E 2](/2022/05/25/dall-e.html) when it first came out, to [collecting others' examples of open-ended exploration](/2023/03/06/open-ended-exploration.html), and a [computational creativity conference paper](https://arxiv.org/abs/2205.01605). And of course lots of related discussion on [whether computers can be artists.](https://www.mdpi.com/2076-0752/7/2/18)

This post summarizes the results of those explorations. My answer won't be surprising to anyone who's read my writing or speaking before, but here I'm putting together those ideas into a coherent statement on computational creativity.

Now, this discussion would be easy if we had a clear, concrete definition of "creativity." But we don't. We have intutions, and we have the way the word is used (which, according to Wittgenstein, _is_ meaning), and lots of previous attempts to define it. Our definitions don't tell us anything about machine-made creativity because we haven't ever considered machines as creative before.

In fact, the new technology helps us attempt to clarify what is or isn't "creativity," by providing provocative real-world examples.  Just as new technologies do with "art," another word for which there are [no simple definitions](/2022/09/19/art-definitions-1.html), but many usages.

_Note: since writing this post, I've come across a lovely paper by Lindsay Brainard that expresses many similar ideas to those here: [Paper](https://www.tandfonline.com/doi/full/10.1080/0020174X.2023.2261503), [preprint](https://philpapers.org/rec/BRATCC-9)._


# "Creativity" as "Making Creative Things"

Many attempts to define _creativity_ describe [making something good that didn't exist before that's particularly surprising and unique](https://onlinelibrary.wiley.com/doi/abs/10.1002/jocb.516).  An artist makes a painting that's particularly provocative or beautiful in a new way, or expresses a new visual idea. A writer composes an unusual story with a surprising take. A research paper suggests an unexpected new approach to an old problem, or an unexpected but exciting new problem.  

So, a lot of effort goes into defining what makes a painting or an invention "creative."  Past authors distinguish between "little-C" personal creativity, such as a child's drawing, and "big-C" innovative creativity that affects society, such as a highly-original fine art painting or invention.

A natural next step, then, is to say that "creativity" _only_ requires that the product is creative. Many computer scientists have gone this route, sometimes running studies to ask viewers to rate the "creativity" of algorithmic outputs and comparing them to human-made products. In part, this might be because [many "AI" researchers love quantification and benchmarks](/2020/10/21/quantitative-evaluation.html), perhaps even suffering from the [McNamara Fallacy](https://en.wikipedia.org/wiki/McNamara_fallacy). If a machine makes an outputs that people rate as creative, then, it is reasoned, the machine itself must therefore be "creative."

But, in that view, we _already_ have creative systems—and we've had them for decades, even if they've been more "little-C" than "big-C". We have decades of high-quality generative art that, though human-authored, can autonomously generate new works. [Harold Cohen built a system called AARON](https://en.wikipedia.org/wiki/Harold_Cohen_(artist)) that automatically produced many abstract and figurative artworks, shown in major galleries and museums.  And, even simpler, [the Mandelbrot set](https://en.wikipedia.org/wiki/Mandelbrot_set#Computer_drawings), produces a seemingly-endless stream of mesmerizing imagery:
<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/b005iHf8Z3g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>
that, surely, no one (including Mandelbrot himself) could have predicted from the math itself.  In fact, [chaos theory](https://en.wikipedia.org/wiki/Chaos_theory) tells us that it is unpredictable. Yet it can be described in [a single equation](https://en.wikipedia.org/wiki/Mandelbrot_set#Formal_definition), or [a few lines of code](https://en.wikipedia.org/wiki/Mandelbrot_set#Computer_drawings). 

And, arguably, so many of our video games produce novel images and experiences procedurally. Sure, people authored them to generate these experiences, but people have also authored all of our current "AI" systems.

# Productivity or Humanity?

People in the 20th Century studied creativity for at least two distinct reasons:

1. First, [business leaders sought to **increase corporate productivity.**](https://www.newyorker.com/magazine/2023/04/24/the-cult-of-creativity-samuel-weil-franklin-book-review) 
Management researchers and psychologists tried to understand how companies come up with new product ideas, solve problems, and make effective new ad campaigns. How did creative individuals and teams function, and how could they be made more effective?  

2. Second, psychologists sought to **describe human intelligence and behavior**, and to improve it. What are the attributes of creative behaviors and creative people? How can psychologists help people explore their own creativity and, thus, their own self-actualization?

These distinct goals persist in how we talk about creativity in "AI" today. 

If all you care about is productivity and problem-solving, then, indeed, the output is all that matters when defining creativity. Can the system create useful new things?

If so, then, by that definition: of course computers are already creative, and _have been for decades_, as in the examples in the previous section. And they're getting better and better at it.

But I don't think that's what most of us mean when we ask whether algorithms can be creative. 

**In this essay, I'm focused on how the systems we build relate to human creativity and intelligence.**   When we say that an "AI" is creative, then we're saying it's creative in some way similar to human creativity. 

I do not think that just looking at the outputs is enough.  Computer systems work by following instructions, and I think most of us would agree that human "creativity" can't just be about following instructions. 

Imagine hiring an employee to create a Spanish-language poem, by following very specific rules. Your employee-who doesn’t understand Spanish-must follow the rules precisely, to the letter, without deviation. The rules might be very complicated and involve rolling dice. In the end, your employee produces a poem that is widely lauded as original and wonderful. Is the worker "creative"? I think most people would say no. 

But this is exactly a description of how computers work: they follow instructions they were given precisely, without deviation. (This is a variant of the ["Chinese room argument"](https://en.wikipedia.org/wiki/Chinese_room)). Precisely-following instructions without deviation or autonomy does not seem "creative" to me.

<center>
  <figure>
<iframe width="560" height="315" src="https://www.youtube.com/embed/zNB3cr-3Gi0?si=q7DeNYvMCG9Rpj6s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
<figcaption><i>Surely there's more to creativity and discovery than following instructions.</i></figcaption>
</figure>
</center>

# Computational systems as _models_ of intelligence

What then, are we to make of the fact that current systems can create surprising, novel, and delightful things? That the latest text-to-image systems can make pictures that, had they been made solely by a person, we'd certainly call "creative?"

When comparing to human intelligence, or the intelligence of other animals, we should think of "artificial intelligence" algorithms as _models of aspects of animal intelligence_.  In science, we often must choose between models that capture phenomenology well and models that capture aspects of the underlying mechanisms.  Hummingbirds and helicopters can both hover, but a helicopter is a poor model for the workings of a hummingbird, or its intelligence. 

"AI" models are optimized and trained to model the phenomena of human dialogue and picture-making—and they often do so very well—but the underlying mechanisms are almost entirely different. In nearly ever layer—biology, system dynamics, evolutionary, social, and cultural history—human intelligence is entirely different from "AI."

I often hear "we're just computers"; aren't [we all just consequences of the laws of physics](https://en.wikipedia.org/wiki/Determinism)? [But we're not _just_ computers](/2022/09/04/computationalism.html) in the sense of our current understanding of computation; this false equivalence [confuses two different very notions of computing](https://www.frontiersin.org/articles/10.3389/fcomp.2022.810358/full).

It's fine to say that our current algorithms are "intelligent" as long as we understand that this "intelligence" describes a set of skills, rather than representing a holistic model of human or animal intelligence.

Likewise, "computational creativity" algorithms can _model_ aspects of how human creativity works.  We have all sorts of [computer graphics](/2020/09/12/how-to-draw-pictures-contours.html) and "AI" algorithms that make novel and original pictures, and can fool people and be judged artistic in some sense, but they all do so by following their instructions.

[Psychologists have pointed out many aspects crucial to human creativity](https://onlinelibrary.wiley.com/doi/full/10.1002/jocb.395), almost none of which our current algorithms attempt to model.



# Creative processes

Our current algorithms do not attempt to model the _processes_ of human creativity. Here's one important aspect that I think is missing.

Simplistic descriptions of creativity often emphasize "inspiration," an instaneous flash of insight, those "where did that idea come from?" moments, perhaps granted by the gods on the subconscious mind.  Hollywood stories like to dramatize invention with a dramatic moment when the scientist or artist saw some real world behavior and turned it into their new discovery.

But these flashes of insight are rare, and there's much more to it. Creativity arises much from a _process_, not just one moment. Often, it's hard work getting to that moment, and hard work after. And flashes of insight aren't necessary for discovery. Often, it's not one big moment, but a series of many small moments.

Even if Kekulé solved the chemical structure of benzene in [a lucky vision of a snake biting its own tail](https://en.wikipedia.org/wiki/Benzene#Ring_formula), it was because he'd spent years studying chemical bonds and working on the problem. 

Think about a few times you made something that you consider creative. It doesn't have to be a great work of art, just something you were proud of, something artistic, or something clever you figured out, or designed. In can just be run-of-the-mill, everyday creativity. In these experiences, how much did you know about what the final outcome was going to be when you started? How predictable was it? And how does that relate to your sense of how creative you'd been?

Here's my experience; you can see if you relate at all.

When I draw or paint a picture, or work on a research project, I can't really predict the outcome.  I usually start a painting with a vague, initial idea for what it should be. Then I start working, and, as I do, something starts to emerge. It's usually different than what I'd imagined... and, often, better. So I keep working on the new thing, but, rather than try to bring it back to the original idea, I try to make the new thing work. I end up something that I hadn't thought of before—something that hadn't even occurred to me as a _possibility_ before.  It wasn't the initial idea that made the work—although sometimes the initial idea is a big part of it—_the creative idea was discovered through the process of working_.

The more predictable the outcome, the less creative it feels. If I walk into the kitchen without a plan for what to cook and combine ingredients a bit differently than I have before, it only feels slightly creative. If I paint a picture that ended up totally different than I'd originally meant, that feels much more creative.  Of course, a picture can still be skillful without feeling as creative.

**It's not just me.** The more I started to understand creativity this way, the more I recognized it in artists' descriptions of their own practice. Reading [_Why Greatness Cannot Be Planned_](https://link.springer.com/book/10.1007/978-3-319-15524-1)  helped too. 

[This blog post](/2023/03/06/open-ended-exploration.html) collects many examples I've found of great artists describing their practice in terms of this kind of process of discovery.

Moreover, I bet that if you probe any competent creator, you'll discover a refined practice of developing ideas, following intuitions and gut feelings, and explorations and refinements that helps them make these discovering.  Learning to be creative involves learning many specific skills and intuitions.

In short, creativity isn't just about what you produce. It's how you got there.

As a result, really creative works aren't just surprising to the audience... really creative works are surprising to the person who made them.


# Goals: open-ended or well-defined

Another attribute of human creativity that's missing from computational systems is its open-endedness.

A big part of the creative journey for me, and for many people, is redefining goals. I start out meaning to paint in one style and end up with a different kind of painting. I intend to solve one research problem, and end up publishing a paper on another.

It isn't just me. So many great artists and researchers [start from an initial vague idea, and then evolve or discard that idea while working](/2023/03/06/open-ended-exploration.html).  **Many great inventions come not from picking a problem and solving it, but from figuring out the problem and the solution _together_.**  Over and over, artists and researchers describe their processes this way.


But sometimes the solution to a well-defined problem is described as creative, especially lateral-thinking solutions that bypass unstated assumptions. For example, advocates for computational creativity seem to frequently quote Go champion Lee Sedol's description of one AlphaGo move in 2016 as "creative." This quote gets trotted out again and again as evidence that computers can be creative, including in discussions of artistic creativity. Solutions to optimization problems themselves are also [described as creative](https://arxiv.org/abs/1803.03453).  I can attest that it does feel magical and lifelike when [an animation control optimization produces its own delightful behaviors](https://www.youtube.com/watch?v=9pGH6-QY-sQ). But, when the results are surprising, I would call these results unintended consequences of the design of the loss function or constraints.  

In my opinion, there are important differences between [open-ended problems](/2023/03/06/open-ended-exploration.html), and problems where there is a concrete goal or objective function. Open-ended problems include things like "make an artwork," "invent something new," and concrete goals are "solve a math problem" or "win a game of Chess or Go."   Solutions to both may be described as "creative," but they aren't the same thing.





# Toward new kinds of models

Could we formulate computational models of the processes of open-ended creativity?  In [my ICCC 2022 paper](https://arxiv.org/abs/2205.01605), I proposed a model for open-endedness computational creativity that generalizes optimization. I'm not sure if the model can be realized. But, even if it can, it would still just be a different computational _model_ of creativity.

Ultimately, all of our algorithms are still just going to be algorithms, sets of instructions for computers to make things, and sometimes they will mimic well the phenomena of human creativity, and in other ways they won't.

<hr>
<i>Thanks to Laura Herman for comments on this piece and sending links that made me rewrite parts of this.</i>