---
layout: page
title: Computer Science Venues Should Publish Position Papers
summary: We should have peer-reviewed venues for discussing our fields.
author: AaronHertzmann
---


# Computer Science Venues Should Publish Position Papers


Research continually reinvents itself: the important problems and directions continually change; moreover, in the past decade, the ways we do research and publish continually change, as has the impact of computer science research on society. But, in the computer science venues where I spend most of my time (computer graphics and vision), we don't really have published forums for discussing these things.  Discussion happens in separate channels and social media, and so it doesn't reach or involve the whole research community.

I think we should: we should have peer-reviewed Position Paper (or "Meta Paper") tracks within our main conferences and journals.  Traditional scientific venues have many such kinds of publication, e.g., Letters to the Editor, [Perspectives](https://www.science.org/doi/10.1126/science.adh4451), Review papers, and others.  We should too.


# People have opinions, but the discussions aren't shared

Research leaders and up-and-coming junior researchers have a lot of opinions and ideas, views on where the field is going, where it _should_ be going; or where it is failing and how to fix it. These opinions sometimes appear on social media. Historically, most of the in-depth discussion happens at conference workshops, invitation-only workshops in sunny European resorts attended by a select few, or at dinners and drinks during meetings.  Many people even prefer these workshop talks to the talks at the main conference. But, the content of these presentations are rarely written down or shared (apart from an occasional hard-to-watch Zoom link); they are seen and heard only by a lucky (and, often elite) few.  It's a matter of luck whether you happen to have heard someone's inspirational vision for where the field should turn next, which is especially important right now when there's so much upheaval.

For example, I've heard many debates over the years about whether labels are ultimately necessary for computer vision, whether and how they can even be defined, and what alternatives there might be. But, if you read the literature in the field (and [the criticisms from outside](https://excavating.ai/)), you might think that everyone believes that labels are necessary and uncomplicated. And now, as the fields begin to have much broader societal impact, new debates around the ethics and consequences of these impacts emerge as well. 

All of these different venues have their own value, but none of them is simultaneously (a) published, and (b) coexisting alongside the main conference, and (c) careful, thoughtful, and scholarly. For example, social media is good for hot takes and rapid discussion, but often turns nasty and shallow, and many researchers simply do not follow it.  [CACM](https://cacm.acm.org/) provides for these kinds of discussion, but it doesn't support the kinds of discussions we want in specific fields.


# What Position Papers Are

There are many kinds of publications that I'm lumping together under the name "Position Paper." But they share the following features.

**A Position Paper presents a point-of-view, synthesis, or other scholarly perspective on a research field. It may be opinionated, but should be carefully-reasoned and supported by appropriate citation, in a manner accessible to members of the relevant research community.
Position Papers are peer-reviewed papers that appear in a separate track within the same conference as the field they're commenting on.**

A position paper may cover any topic relevant to the research field, such as:

* Directions researchers haven't focused on but should (e.g., embodiment, AI as tools vs. creators, uses of language and vision)
* Methodological problems that should be fixed in papers, e.g., [use of user studies](https://arxiv.org/abs/2206.11461), ethical practices
* Review processes and conference/journal formats (e.g., arXiv ban, new conference tracks)
* Broader context and societal impact, and how it should affect research publications
* Blind spots in the literature, and how to correct them
* Reinterpretation of existing results with a new theory

A position paper should not just be science fiction ideation ("what if we figured out how the brain does vision?") nor should they be angry rants. They may be fantastical or opinionated, but they should be supported by careful reasoning and citation, and they should provide novelty, i.e., new insight and depth.   For example, a paper shouldn't just complain about single-blind or double-blind reviewing, and stupid reviewers; it should construct an argument one way or the other, drawing on the extensive literature and studies on these topics, and even the author's own experience, weighing the benefits and harms of each. Papers should be specific to the field where they are published (e.g., not just about double-blind reviewing in general).

Position papers should be accessible to researchers in the relevant community.  When bringing in ideas from other fields—whether from X-ray crystallography or critical race theory—unfamilar terminology and concepts should be defined in an accessible manner.  Authors expressing controversial views should make an extra effort to be understandable and persuasive to a broad audience, e.g., acknowledge, respect, and respond to differing views—but without diminishing the force of their own views.

Position Papers should have their own reviewing tracks and reviewing standards. Single-blind reviewing should be the default, since the identity and direct experiences of the authors may be an important part of the paper (although perhaps authors could be given the option of double-blind).  A senior author with experiences across many parts of the reviewing process would be read differently from those of a new researcher (and both can be valuable).

Position Papers can be cited like any other paper. They can be useful when writing a paper when you need to motivate the problem or the approach. For example, I've published papers on physics-based character animation and tracking at various times, and often we need to argue why this is a worthwhile research area (especially back in the early 2000s when physics-based animation was out of favor), and arguing for different evaluation metrics (since the evaluation metrics often used in vision don't measure the right things).

Survey Papers are not position papers if they merely summarize published work. But Position Papers frequently survey and summarize the literature in support of the point they make; Position Papers often have very long lists of references.


# Why Write One?  Why Not Just Blog Posts and Tweets?

**Publishing position papers incentivizes academic researchers because, unlike blog posts and tweets, they have the usual rewards of peer reviewed papers: you get the benefits of having published a paper, adding lines to your CV and citations. But, more importantly, they give you an outlet for your ideas and vision, a chance to influence thinking in the field and be recognized for it.**

I was spurred to write this post by the plenary and workshop discussion at CVPR 2023, where people tried to share visions about how computer vision research should proceed given recent upheavals in the field. If you didn't attend these talks, then you probably don't know what people said. In one plenary, Sara Beery pointed out that NeurIPS created incentives for different kinds of research by creating a dataset paper track. So I thought: why not a Position Paper track?

In my experience, there's a big difference between writing some Tweets, writing a blog post, and writing a real paper; each has value. Blogging is good for getting an initial set of ideas out there, without putting too much pressure on yourself.   Writing things down forces you to think through your ideas—**you learn a lot by writing things down**.  Writing a real paper requires polishing the ideas even more. And, you learn a lot by seeing what anonymous peer reviewers say—even if you initially think the peer reviewers are nuts, their feedback is still useful.  

The good things about blogging is that you don't need to careful edit or to cite all the related work and studies.  The good thing about publishing papers it that you have to carefully edit your text and carefully cite all the related work and studies.

Position Papers may even be useful for historians of science, to understand what the researchers were thinking at the time, and not just what methods ended up being adopted. I've recently read several criticisms from outside these fields purporting to explain what CS researchers believed about the world based on the epistemology embedded in our models: while the criticisms of the models are valid, the descriptions of the pioneers' beliefs seemed to have been invented from whole cloth. Yet, there were no public writings to show otherwise. 




# A Few Concrete Examples


HCI as a field does seem to have several Position Paper traditions. One paper I keep returning to is ["Usability Studies Considered Harmful"](https://www.billbuxton.com/usabilityHarmful.pdf) by Saul Greenberg and Bill Buxton. This paper presents a detailed, coherent argument against overreliance on user studies. I came across it years after it was published, and it provided me with useful guidance and insight, and supported my suspicions that user studies could be overdone. 

The last few years of the NPAR conference introduced a Meta paper track. Only a few Meta papers were published, but my own 2010 paper ["Non-Photorealistic Rendering on the Science of Art"](http://www.dgp.toronto.edu/~hertzman/ScienceOfArt/) is one I'm quite fond and proud of, advocating a point of view quite beyond what most people in the field were pursuing at the time: a vision for NPR as a part of scientific research, not just making pretty pictures; in the section on user studies, I cited Greenberg and Buxton. The paper was useful for consolidating some of my own thinking, although I wasn't ready to act on these ideas until years later.

My 2003 invited paper arguing for [the use of machine learning in computer graphics](http://www.dgp.toronto.edu/~hertzman/mlcg2003/) is something of a time capsule, pointing to a time when ML use in graphics was extremely rare, including quotes from colleagues saying that machine learning doesn't really work; the Bayesian stuff was not so useful, in retrospect.



**Review papers.** 
One interesting case are "review papers" in scientific fields.  I've only learned about this category recently (as I am currently preparing a review paper), and realized that many of my favorite scientific papers are reviews. The Journal of Vision defines a review paper as "Reviews are meant to sum up the current state of the research on an important topic and are regarded as being the first place to get authoritative information about that topic. They should contain new insights on the topic or provide a new synthesis of data."

Some of my favorite scientific papers are essentially review papers/Perspectives, such as [Rosenholtz on foveal and peripheral vision](https://rdcu.be/b0EWf), [Yamins and DiCarlo on neural network models of the brain](https://www.nature.com/articles/nn.4244), or classic examples on reproducible science like [Simmons et al on False-Positive Psychology](https://journals.sagepub.com/doi/10.1177/0956797611417632) or [Ioannidis on why most published studies are false](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.0020124).  I would argue that papers like these, which are extremely valuable and often influential, could not find homes in our CS venues.  (My own papers on [line drawing perception](/2021/05/13/why-does-line-drawing-work.html) could fit into these categories as well, as they do not include new experiments or algorithms but instead reinterpret existing results.)

Incidentally, I would support seeing more "review papers" in [FnTCG&amp;A](https://www.nowpublishers.com/CGV) ([our recent paper on user studies](https://www.nowpublishers.com/article/Details/CGV-106) might fit into this category, although it wasn't conceived that way).

