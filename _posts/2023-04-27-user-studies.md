---
layout: page
title: The Curse of Performative User Studies
summary: Why user studies in graphics and vision are (probably) often wrong, and what we can do about it.
author: AaronHertzmann
---


# The Curse of Performative User Studies


Anyone who has spent enough time publishing some kind of artistic tools in computer graphics—even [in computer vision conferences](/2020/08/31/cvpr-graphics.html)—has probably gotten reviews that praised a paper's ideas and results, but required a user study. Or the reviewers didn't like the paper's methods or results, but still said the authors should add a user study.   And so, maybe you added user studies to your next paper _solely_ because you believed reviewers would require it. 

As an author, reviewer, and PC member who works in more "artistic" subjective subfields, I have experienced or witnessed cases like these many times in the past few years.  So often, the user study seems unnecessary or even useless, just a waste of everyone's precious time.  

I suspect many studies published in graphics and vision are **performative, not informative**: we do them not because we want to learn something, but solely because reviewers expect to see a study. So we put on a show, a performance.

Some subfields, including animation and tone-mapping, do have long traditions of rigorous, worthwhile studies, as does the field of HCI.  For example, I think Forrester Cole's work on [making](https://gfx.cs.princeton.edu/pubs/Cole_2008_WDP/index.php) and [perceiving](https://gfx.cs.princeton.edu/proj/ld3d/) line drawings are quite significant, high-quality perceptual studies.  This post isn't about those lines of work.  This post is about the performative user studies that have become common since the advent of crowdworking in 2008.  Crowdworking made gathering numerical scores easy, by allowing researchers to treat human individuals as algorithmic data sources.

**We need a better understanding of if, when, and how user studies are valuable.** When done thoughtfully, user studies can provide invaluable insights and new information, even leading you to new research ideas. 
[As we describe in a recent paper](https://arxiv.org/abs/2206.11461), the best user studies take time and effort, and often don't involve crowdworking or quantification at all. But, in much of graphics and vision, the growth of crowdwork has diluted the concept of "user study" to the point of meaninglessness. User studies are often considered necessary for publication, but few standards—if any—seem to govern how these studies are conducted.  **In this piece, I'll provide some recommendations for what we can do about it.**





# An example of bad reviews

[Here's an instructive example from ICLR 2022](https://openreview.net/forum?id=oapKSVM2bcj) where two reviewers justified low scores, in part, because of a lack of user studies. In response, the Area Chair wrote:

<center>
   	<a href="https://openreview.net/forum?id=oapKSVM2bcj">
   <img src="../../../images/iclr2022-decision.jpg" alt="ICLR decision excerpt: &quot;I belive it is fair and measured to state that these reviews may be considered to exhibit aspects of gatekeeping: requiring more &quot;mathiness&quot; that does not help the paper, or more &quot;rigour&quot; through user studies that are in fact less valuable than the reviewers' own observations &quot;I could see myself...&quot;, &quot;I tend to buy...&quot;.&quot;"/></a>
</center>

To this anonymous Area Chair, I say "Bravo." 

If this sounds weird, I recommend reading [the Paper Decision and reviews](https://openreview.net/forum?id=oapKSVM2bcj) and then thinking through what user studies the authors could have actually performed, and whether they would have been genuinely meaningful or necessary.  Would the author—who does not appear to be academically-employed—have had the time, energy, and expertise?  Moreover, this Area Chair had outside knowledge of the system's impact—would they have rescued the paper otherwise?

I've seen and heard of so many similar examples of reviewers tossing off the phrase "you should have a user study" without any apparent thought.

Some user evaluation requests are even more ridiculous. One colleague at Pixar complained that reviewers rejected his paper because he'd not had animators make a professional animation with the system—essentially, the reviewers were asking for a multimillion dollar production.  Even in the CHI community people complain about [evaluation requests that would require _years_ of extra effort](https://dubfuture.blogspot.com/2009/11/i-give-up-on-chiuist.html).  It's unclear that reviewers have really thought through the effect of what they're asking for.


Two pitfalls
=====

I think there are two particular common pitfalls in papers:

**Pitfall 1 (_Foregone conclusions_):** The results in the paper figures are good enough that obviously the method is better, and a user study is redundant. This is probably the common case among _accepted_ papers. The study was just a bunch of unnecessary extra work.

**Pitfall 2 (_Replicability_):** The method isn't very good, but the user study shows it is.

I think the former pitfall is straightforward; I propose later cases where such a study could be useful as a "sanity check" on the figures.

The latter pitfall requires more explanation.


Replicability pitfall: a story
=====

Here's an in-depth example from a recent project, that ought to unsettle anyone that uncritically relies on crowdworker studies.  

A few years ago, some artists began making art by [manipulating Generative Adversarial Networks (GANs) to produce weird-but-intriguing outputs](https://direct.mit.edu/leon/article-abstract/53/4/424/96926/Visual-Indeterminacy-in-GAN-Art?redirectedFrom=fulltext), rather than the realistic-but-plain-looking images that GANs normally made. They "looked like" Modern Art, especially much of the weird and surreal art from the early 20th Century; why?

Inspired by GAN art, [we developed a way to quantify](http://cybertron.cg.tu-berlin.de/xiwang/tap-project-page) the ["indeterminacy"](https://www.frontiersin.org/articles/10.3389/fnhum.2011.00084/full) of an image.  Here's our quantification on some GAN images from [Artbreeder](https://www.artbreeder.com/):

![high and low entropy images](../../../images/image-entropy.jpeg)

To us, the bottom row looks the most interesting and artistic, so the numbers roughly match our judgement how interesting the images is. 
The reviewers of [our paper](http://cybertron.cg.tu-berlin.de/xiwang/tap-project-page) agreed.  Moreover, previous psychology studies have shown that more ambiguous and indeterminate images tend to be more aesthetically interesting. So we had every reason to expect that a more formal study would show the same thing.

**But it wasn't so easy.** We began a new project, paying crowdworkers to rate how much they liked these images.  And the results weren't what we expected: crowdworkers preferred the boring pictures. They preferred kittens and mountains, not indeterminacy. 

We imagined many explanations. Maybe it takes too much time to really appreciate indeterminate artworks, and crowdworkers were just speeding through the tasks to get paid. Or maybe they just don't like Modern Art. 

So we devised different versions of the tasks, giving the workers different questions to answer ("which images are most interesting" or "artistic"), and  different ways to do the ratings that would make them slow down. Each time, the crowdworkers preferred mountains and kittens. 

We finally obtained the results we expected both by changing the task structure, and by analyzing the data differently. Most importantly, we found that only a significant subset of crowdworkers did consistently prefer indeterminate artworks.  We've written [a paper](https://psyarxiv.com/nd653)  describing all these steps (and validating on hold-out data) that has been accepted to appear in [a psychology journal](https://www.apa.org/pubs/journals/aca). 

**So, consider the following**: 

1. We used crowdworking methods common in graphics and vision, and
2. Different experiments gave opposite conclusions. 

We could have just reported the results of our final study. This would have made our paper much more impressive and exciting.  But this would have been misleading, and, arguably, unethical.  Instead, we were open to learning something from these studies, and so we tried many experiments, and reported all of our findings, which will hopefully inspire future studies to disentangle all the factors we identified.

But I wonder how many published "user studies" in graphics and vision were performed this way: keep running crowdworker evaluations until you get the result you want, _only_ publish that final evaluation, and then declare victory.


The Replication Crisis in Psychology
========

This story exemplifies a broader theme in science. For more than a decade, psychology, medicine, and other scientific fields have grappled with [The Replication Crisis](https://en.wikipedia.org/wiki/Replication_crisis): the observation that many published scientific studies are probably false, and/or could not be replicated in independent trials.   [One large scale psychology study probing the problem](https://www.science.org/doi/full/10.1126/science.aac4716) replicated _only 35%_ of the 100 papers they tested. Results like these led to widespread [changes to publishing policies in psychology](https://en.wikipedia.org/wiki/Replication_crisis#Remedies), including the use of [preregistered studies](https://en.wikipedia.org/wiki/Preregistration_(science)) and reforms to how experiments are described.

What causes this problem? [One influential 2011 paper](https://journals.sagepub.com/doi/full/10.1177/0956797611417632) details ways that experimenters can bias results towards the results they want, even unconsciously.  For example, running many studies but only reporting the successful ones creates a problem called [publication bias](https://en.wikipedia.org/wiki/Publication_bias).

If rigorous scientific experiments have gone through such an upheaval, shouldn't we wonder about some of our own experiements? Indeed, there have been related concerns raised of a [replication crisis in computer science](https://cacm.acm.org/magazines/2020/8/246369-threats-of-a-replication-crisis-in-empirical-computer-science/abstract) and in [machine learning](https://reproducible.cs.princeton.edu/), as well as evidence that [dataset bias](https://people.csail.mit.edu/torralba/publications/datasets_cvpr11.pdf) leads to results that [do not generalize well](https://proceedings.mlr.press/v81/buolamwini18a/buolamwini18a.pdf).  (Note that the easily-confused terms "reproducibility" and "replicability" [are sometimes swapped in their meanings](https://www.frontiersin.org/articles/10.3389/fninf.2017.00076/full). I'm skipping over the precise meanings here.)

If that's not concerning enough, consider this. Crowdworking on MTurk grew popular for user studies after a series of studies in [HCI](https://dl.acm.org/doi/abs/10.1145/1357054.1357127), [visualization](http://vis.stanford.edu/files/2010-MTurk-CHI.pdf), and [psychology](https://journals.sagepub.com/doi/10.1177/1745691610393980) showed that crowdworking gave similar outcomes to in-person studies. But, there's some evidence that [the reliability of MTurk data has _gone down_ over the years](https://journals.sagepub.com/doi/abs/10.1177/1948550619875149).



If There's A Crisis, Would Anyone Care?
=====

All of the above **leads me to believe that most "user studies" in computer graphics and vision are not replicable:** they would not hold up if someone tried to redo the study with new participants.  In fact, they're not even reproducible, given that few authors provide complete details about their methodology. In other fields, recognizing this would lead to a wake-up call, a need to reform publication practices. 


[I've complained about performative user studies many times before](/2020/10/21/quantitative-evaluation.html). But most people (with a few exceptions) don't seem particularly concerned about whether or not our studies are "true."

Suppose we ran a large-scale study _about studies_, and found that many of our published user studies don't hold up. Would we care at all?  After all, we're not building psychology theories around these studies, and [turning them into TED Talks and best-sellers](https://www.nytimes.com/2017/10/18/magazine/when-the-revolution-came-for-amy-cuddy.html). The outcomes of our studies are largely ignored once the paper is published.  

(One important consideration I'm glossing over is whether we'd want to judge replicability among crowdworkers or among a different pool of participants. Our crowdworker studies may technically be replicable because they can have large sample sizes, but there may be important other problems with the study.)

But, if no one cares, isn't that a sign that these studies don't matter?  



What Should We Do About It?
=====

There are a few things we can do about this problem.

**Stop requiring performative user studies**

At the very least, don't just say "you should do a user study," without specifying precisely the purpose of the study and how it would be conducted. Is asking crowdworkers which pictures they like better really meaningful in this case? How might the outcome of the study change your evaluation of the paper?  If not, why are you asking for the study? Explain these things in your review.

Some people respond to this with: "OK, but then how should we evaluate papers without benchmarks?" This question presumes that [objective, quantitative evaluation is somehow necessary for publication](/2020/10/21/quantitative-evaluation.html).  Or, worse, that _any_ metric—even a bad one—is better than no metric at all.

Focusing only on quantitative metrics falls into the [McNamara Fallacy](https://en.wikipedia.org/wiki/McNamara_fallacy): making decisions solely based on what we can measure numerically, and disregarding all other considerations.  

**Resist performative user studies**

* As an Area Chair/committee member, push back on reviewers that ask for performative user studies.
* As a reviewer, don't accept papers just because they have a user study; question whether the user study is meaningful, just as you might with other quantitative evaluation.
* As an author, resist calls for performative user studies. Feel free to link to this blog post, and/or the papers listed below.
* Conversely, be accepting of qualititative user studies that can provide information that quantitative studies lack.

_"You should do a user study"_ should be treated like _"This method is not novel"_:  You can't just say either without explanation.


**Report results carefully**

Describe your study protocol carefully. Don't over-generalize from the results.  [The way you design your study can really influence your results](https://www.sciencedirect.com/science/article/pii/S2589004220307070) and so the formulation needs to be clear in the paper.


**Accept that reviewing is a judgement call**

At a high-level, we first need to **accept the fact that paper decisions are subjective** and involve judgement calls.  In the top computer science conferences, we review papers based on whether [_we think the paper will make a positive impact._](/2020/07/13/rebuttals.html) This is why we reject many papers for no particular flaw other than not being very "novel" or "interesting." 


We also need to recognize that _almost no graphics or vision paper evaluates with real applications in real deployments_.  [All our datasets and benchmarks are approximations to what a real practitioner might care about](https://arxiv.org/abs/2107.07002), and sometimes [they might be poor approximations](https://proceedings.mlr.press/v81/buolamwini18a/buolamwini18a.pdf).  

The "users" in our so-called "user studies" are almost never actual users of the proposed system.

Hence, reviewers must make judgement calls about whether the ideas and results are valid, interesting, and worth publishing. User studies can help with these judgments if done well, but, more often, they're just a box to check on a form.

**Accept that studies are often ambiguous**

I experienced first-hand the ambiguity in study data with our [2011 paper on color compatibility](http://www.dgp.toronto.edu/~donovan/color/).
For years, psychologists had used limited in-person studies on simple pairings to measure color compatibility on just a few subjects. We began thinking that big datasets and crowdwork would allow us to figure out much better which colors go best together. 

Each time we formulated another study or data analysis, we thought it might answer basic questions, like which color theories worked better.  And, with each study we ran, we realized there were multiple explanations for the results.  Maybe the results depended on the background color when viewing the ratings. Maybe the fact that some data sources came with titles affected the ratings.  We would then devise tests to separate factors (e.g., with and without titles), and each of these led more questions, and an endless rabbit-hole of confounding factors.  

During this process, a colleague Ryan Schmidt, who published frequently in HCI, commented that reviewers could poke holes in any study. If they did a line drawing study on paper, reviewers would complain about which kind of paper was used and whether the study generalizes to other drawing media.

Doing science means acknowledging and understanding the limitations of your studies. No user study on its own is conclusive, but some are better than others.


**Consider crowdworker evaluations as "sanity checks"**

One possible mental model for crowdworker evaluations is as _sanity checks_: they check whether the results in the paper figures generalize to a larger dataset. 

Reviewers should judge the results in the paper figures, but these results might be cherry-picked, and a crowdworker study can expand that evaluation.

Conversely, if the reviewers believe in the value of the paper just based on the ideas and the figures, then no study is necessary. If the reviewers do not believe in the value of the work, then no crowdworker study will change that. 


**We need new research: studies about studies**

Finally, I think we need new research to formulate better guidelines. This is an open research problem, that people in our community should pursue.  We could draw inspiration from how other fields have responded to the Replication Crisis, although the solutions might be different.  

Here are some of the kinds of research questions that I hope someone will tackle:  

* Are existing studies meaningful (Pitfall 2)? Pick highly-cited recent papers with user studies and redo them in some rigorous way. 

* Most likely, many of those results will hold up. But there's a second question: was the outcome obvious just from the figures in the paper (Pitfall 1)? That is, a second study would be: compare readers' evaluations from the figure papers alone to a larger scale user study. In short, does the user study add anything beyond the figures?

* Can we form more specific guidelines around how to perform studies, e.g., how does rendering style and display size/context affect results?  For example, you can't compare character animation results with just stick figures floating in space.

* Do different problem domains require different standards or guidelines? Judging the quality of a denoising result might be much easier than evaluating indeterminate aesthetics, which is highly subjective, if not divisive.

These ideas need refinement, but they give some idea of the kinds of questions someone could tackle to advance research in our fields.   (I don't plan to pursue these ideas, but I'm open to collaboration).



Further reading
======

In-depth discussion of user studies in graphics and vision, how to improve them, and use other techniques for user research:

* Zoya Bylinskii, Laura Herman, Aaron Hertzmann, Stefanie Hutka, Yile Zhang. [**Towards Better User Studies in Computer Graphics and Vision**](https://arxiv.org/abs/2206.11461), to appear in _Foundations and Trends in Computer Graphics and Vision_, 2023.  

An influential, eye-opening survey on the ways that researchers can cheat when doing studies, even unintentionally:

* Joseph P. Simmons, Leif D. Nelson, Uri Simonsohn. [**False-Positive Psychology: Undisclosed Flexibility in Data Collection and Analysis Allows Presenting Anything as Significant**](https://journals.sagepub.com/doi/full/10.1177/0956797611417632). _Psychological Science_, 2011.

An insightful HCI paper that pointed out many of these issue 15 years ago:

* Saul Greenberg, Bill Buxton. [**Usability Evaluation Considered Harmful (Some of the Time).**](https://www.billbuxton.com/usabilityHarmful.pdf) CHI 2008. 

How working with real users can inform and drive good research in computer graphics:

* Maneesh Agrawala, Wilmot Li, Floraine Berthouzoz.
[**Design Principles for Visual Communication**](http://vis.berkeley.edu/papers/designprinciples/). _Communications of the ACM_, April 2011, 54 (4), pp. 60-69.


