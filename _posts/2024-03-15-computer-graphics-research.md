---
layout: page
title: What is Computer Graphics Research?
author:  AaronHertzmann
image: "/images/wica/bradford_viewers.jpg"
og:image: "/images/wica/bradford_viewers.jpg"
---

# What is Computer Graphics Research?

In this post I propose a view of how to understand computer graphics research. Then I'll mention some limitations of these definitions and philosophy of definitions in general.

Since I started attending SIGGRAPH, I recall people puzzling over what the subject of the conference is. People thought of computer graphics as the study of photorealistic rendering, yet so many other topics became big, like computational photography and non-photorealistic rendering. Since that "post-photorealism" era, [people have occasionally](https://www.youtube.com/watch?v=OqCH66Sgqco) [proposed their own interpretations](https://www.youtube.com/watch?v=Fjrgn67SlWw), as have various SIGGRAPH comittees and mission statements over the years. In this post I propose one idea for that discussion.



# History and definitions

_Note: This section is adapted from a paper that I've submitted for non-anonymous review in a journal._


The nature of computer graphics research has changed over the years. The very earliest computer graphics [focused on line drawing](https://en.wikipedia.org/wiki/Sketchpad).  However, with the availability of framebuffers, research shifted to modeling the physics of light for photorealistic rendering. [Some researchers advocated for](https://dl.acm.org/doi/abs/10.1145/258734.258914)

| <center><b> computer graphics as the scientific study of creating photorealistic imagery perceptually indistinguishable from the real world </b></center> |

The [Cornell Box](https://en.wikipedia.org/wiki/Cornell_box) wasn't just a testbed, it was, arguably, a philosophical statement about the nature and goals of computer graphics research. A considerable body of work today continues to develop both physics-based rendering technologies, and perceptual models of realism.

But much of the early progress was driven by researchers motivated by art and entertainment, and their tools achieved enormous success in the movie and video game industries. These industries cared about artistic usefulness far more than physical or perceptual accuracy. For example, Pixar's core rendering engines are [built on the principles of photorealistic light transport](https://en.wikipedia.org/wiki/Pixar_RenderMan), yet artists employed them to create unrealistic lighting, color, [and movement](https://dl.acm.org/doi/10.1145/37401.37407)---and none of their films could genuinely be mistaken for live-action photography.  The artistic and scientific development of these systems went hand-in-hand---in the words of an early Pixar mantra: "Art challenges technology, technology inspires art."

As computer graphics research matured, it grew to cover all sorts of applications and visual phenomena, whether scientific visualization, painting, graphic design, cinematography, and so on. This raised the question as to how to define the field, since, for so long, "computer graphics research" had been synonymous with photorealistic rendering. Eventually, [a new understanding of the field emerged](https://dl.acm.org/doi/abs/10.1109/38.814562): 

| <center><b> computer graphics research aims to develop new tools for visual art, communication, and scientific visualization. </b></center> |

A paper submission promising completely-automatic image generation would commonly be criticized by paper reviewers for not providing adequate user controls for artists. In this view, we care about photorealism only insofar as it is useful for, say, making movies, or visualizing scientific phenomena. And, photorealistic rendering indistinguishable from reality has progressed to an extent that narrative movies and television use them widely; they are largely inseparable from these art forms.

However, computer graphics techniques have become adopted in other research fields apart from visual art and communication.  I'm most familiar with uses of computer graphics models and ideas in both computer vision and in human vision, both of which have occasionally been described in terms of ["inverse computer graphics"](https://royalsocietypublishing.org/doi/10.1098/rstb.2021.0443). Computer vision regularly uses 3D scene representations developed in computer graphics research.   Some human vision theories build on photorealistic rendering tools, for example, [the idea that human visual cognition uses mental models akin to computer graphics simulations](https://www.pnas.org/doi/abs/10.1073/pnas.1306572110), and theories of [material perception based on computer graphics models].  In my own work, computer graphics ideas have played a key role in my theories of [human line drawing perception](/2021/05/13/why-does-line-drawing-work.html), and of [perception of picture perspective](https://www.dgp.toronto.edu/~hertzman/perspective/).


How can we describe computer graphics research to allow for these scientific uses?  I propose a complementary, third description that makes the relationship to other fields clearer: 

| <center><b> much of computer graphics research aims to develop generative models of pictures and video that look like the kinds of pictures and videos we see in the world. </b></center> |

This subsumes the photorealistic rendering goals (making pictures that look like photographs), but also includes art and design (e.g., making pictures that look like paintings). (In "video," I mean all kinds of moving pictures, including animation and film.)

This new goal might sound indistinguishable from other kinds of scientific modeling, but there are subtle, important differences. For example, simulation of fluids in physics and numerical computing aim for accurate prediction of physical quantities, e.g., to test theories and forecast real systems, such as the weather. Such simulations care about predictive correctness, and often employ massive supercomputer computations to run, without producing realistic animations in the end.  In contrast, [fluid simulations in computer graphics](https://dl.acm.org/doi/abs/10.1145/3596711.3596793) can produce realistic-looking animations very efficiently, often in real-time, even if they give up predictive accuracy by violate physical principles like energy conservation to do so. 

One potential use for these tools is that "AI" tools can [help us understand human visual intelligence and creativity](/2023/09/27/what-is-creativity.html), analogous to the way that [Large Language Models inform understanding of human intelligence](https://journals.sagepub.com/doi/10.1177/17456916231201401) and [convolutional networks inform neuroscience](https://www.nature.com/articles/s41593-019-0520-2).

In short, the goals in computer graphics research are:

* _Engineering/design_: Build useful tools for people to create visual art, communication, and visualization, and
* _Science_: Create generative scientific models of pictorial phenomena, and moving pictures with sound.

These goals overlap substantially, and, in many cases, one can drive the other. I don't think you can describe the scope of the field or its impacts without both.  

**Limitations and missing pieces**

The biggest flaw of my definitions is that they seem to omit some significant topics. Perhaps fabrication fits into my first definition? There used to be a thread of haptics publications at SIGGRAPH.  Some of the work on computational imaging might not fit in easily.  It's normal, of course, to have isolated edge cases (e.g., those papers on tangible user interfaces), if we allow the definition of the field to be fluid. 

Another possible flaw is that human and computer vision are the only other fields that I've identified as using computer graphics models, but surely there are others?

Computer graphics has also contributed to other fields through non-visual algorithms, most obviously through the development of GPUs and [GPGPU](https://en.wikipedia.org/wiki/General-purpose_computing_on_graphics_processing_units) now GPUs are having a huge worldwide impact on many fields. But I don't see this is a continuing theme in graphics research.




# What is a definition and why does it matter?

We first learn of definitions as fixed, static concepts. The dictionary tells you what a thing is, then everything in that category follows that definition. This is the _prescriptivist_ notion of a definition. But, as Wittgenstein pointed out, this isn't how we use words in the real world. If people had been strict about sticking to how they understood computer graphics in the 80s, then it would still be about photorealism, and photorealism only.

Wittgenstein is often paraphrased as saying "meaning is usage:" you can't tell what a word means without looking at how it is used. For example, how would you define the word "game"? He also argued that we can only understanding meanings by looking at ["family resemblances,"](https://en.wikipedia.org/wiki/Family_resemblance) which basically amounts to _[nearest neighbors](https://en.wikipedia.org/wiki/Nearest_neighbor_search) for definitions_. That is, you would categorize a paper by finding which other papers it is most-similar to.

But I think that formulating these definitions is useful—and not just use nearest-neighbors—and to keep updating them as the field evolves.  It's useful because having a definition helps people understand the field. When you formulate the field in this way, it may suggest new directions or gaps in the research. It can help resolve debates about whether a specific paper belongs at the conference.  

Furthermore, having a scientific justification can help with government funding and scientific credibility; these have often been problematic when SIGGRAPH was viewed as just being the R&D arm of the entertainment industry.

These kinds of definitions can overlap with other fields. [The vision conferences now regularly publish computer graphics papers](/2020/08/31/cvpr-graphics.html), another example of evolving goals.  And, I was a little surprised, honestly, when SIGGRAPH 2004 accepted [our image deblurring paper](https://cs.nyu.edu/~fergus/research/deblur.html).

Of course, the most basic, Wittgensteinian definition of SIGGRAPH is "what is interesting to the SIGGRAPH community." It originally baffled me as a criteria for what papers to accept, but now I think this is one useful important meta-definition, since it allows the other definitions to change and evolve over time, by including things that don't seem to fit any of our more-rigid definitions.  The "positive impact" of the paper is probably the meta-definition that I care the most about when reviewing.

Such definitions are naturally unstable. When [the "Escherization" paper](https://dl.acm.org/doi/10.1145/344779.345022) was published at SIGGRAPH 2000, one of my mentors shook his head, saying "What, are we publishing any sort of mathematics without any applications?" and another one, completely independently, said on a different occasion "It's so great that SIGGRAPH is showing that there's room for these kinds of delightful papers."


<hr>

Thanks for feedback from Kavita Bala, Kartik Chandra, and Yael Vinker.
