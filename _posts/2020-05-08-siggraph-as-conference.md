# SIGGRAPH Should Add A Conference Paper Track

Following some recent discussions, here is a revised statement of why I think the SIGGRAPH Technical Papers program should add a conference paper track, rather than being journal-only. In short, **the requirements for publication at SIGGRAPH have slowly become overly burdensome since the switch to a journal-only format in 2003. This hurts authors (especially students), it makes it harder to publish risky ideas, and it's causing a brain drain as SIGGRAPH researchers move to publishing more in other venues.**

I originally [posted about this on Facebook last year](https://www.facebook.com/aaron.hertzmann/posts/10157508064645802); a [subsequent arXiv posting](https://arxiv.org/abs/1911.09197) provoked some discussions recently in private forums. This time I've put it in the form of a bulleted list. See [the Facebook post](https://www.facebook.com/aaron.hertzmann/posts/10157508064645802) for more background on this discussion.

To be clear, I love SIGGRAPH, and it's a great conference. I love attending it, sometimes more than I enjoy attending vision conferences, and I hope to submit a few papers to TOG this year. But I'm publishing in vision much more often these days, and I'm concerned about SIGGRAPH's future. 


The Problem: Expectation Creep
--------------------------

* **The expectations for publishing a SIGGRAPH paper have grown steadily since the switch to a journal model in 2003, and they have become far too burdensome**
* Papers with good ideas get rejected because reviewers demand very extensive experiments and very highly polished results.
* Many of these extra experiments aren’t really necessary
* **Papers are getting longer and longer.**  Twenty years ago, the nominal page _limit_ was 8-10 pages (with exceptions). [Papers are now _averaging_ around 14 pages](https://twitter.com/_AlecJacobson/status/1259526238378561536). This is an unnecessary burden on authors, reviewers, and readers. Some 16 page submissions would have been better as 8 page submissions. (Note that page lengths only started to grow after printed proceedings ended in 2011, and the committee was told to be more relaxed about page length.)
* The second reviewing phase is an additional burden on authors and committee. The committee occasionally requires unnecessary extra experiments. 
* The high evaluation standards do not lead to papers with better ideas. 
	* There have always been plenty of SIGGRAPH papers that are "incremental" in their actual intellectual contribution, but this is not a bad thing
	* Risky papers are harder to publish because [convincing evaluation is more difficult for really new ideas](https://www.billbuxton.com/usabilityHarmful.pdf)
* It was easy to overlook these problems for a long time because SIGGRAPH had no real competition.

_"This is one of the fundamental problems with companies: success hides problems. It happens to a lot of us in our personal lives with our health. When we're healthy, there may be a lot of things that are bad for us, but our health lets us get away with doing stuff that's bad for us. Then years later, the logic of that time doesn't hold up."_ — [Ed Catmull](https://youtu.be/k2h2lvhzMDc?t=801)

Consequences: Brain Drain
--------------------------

* **Researchers are leaving SIGGRAPH when they can publish in vision**. Some of the most significant image synthesis work in the past several years is from SIGGRAPH researchers publishing at vision conferences.  Examples include [neural rerendering in the wild](https://moustafameshry.github.io/neural_rerendering_in_the_wild/), [NeRF](http://www.matthewtancik.com/nerf) (presumably), [StyleGAN](https://github.com/NVlabs/stylegan), [pix2pix](https://phillipi.github.io/pix2pix/), [CycleGAN](https://junyanz.github.io/CycleGAN/), [Face2Face](http://www.niessnerlab.org/projects/thies2016face.html), and [PointNet](http://stanford.edu/~rqi/pointnet/).  
* Trend: SIGGRAPH will become a boutique venue for high-quality papers on geometry, physics, visual interaction, and a few other topics. As each of these topics become more intertwined with learning/vision techniques, they will migrate to the vision conferences, as has already been happening with rendering and geometry.
* While activity in adjacent communities is skyrocketing—e.g., vision, HCI, robotics—SIGGRAPH is flat. Flat isn’t bad, but it’s a warning sign.
* Not every paper has to be a journal paper
	* It's bad for students to only be able to publish one good idea a year in a highly-polished journal format, rather than being able to publish 2-3 good ideas a year in a reasonable conference format.
	* The vision and learning communities are making extremely fast progress in part because they have fast publication processes; things are changing very rapidly, and journal publication is increasingly rare.
* These other venues are not as good at fostering research where we care about output quality and usability, or the fostering community around this research.

Proposal: Add a SIGGRAPH technical paper conference track, similar to what we had before 2002
--------------------------

* Impose page limits, e.g., 8 or 10 pages plus references
* No second round of reviewing
* No change to SIGGRAPH standards in terms of impact/quality of ideas
    * We should be more willing to take some chances on good ideas that may not be evaluated as fully
    * We are not lowering the bar in terms of the quality of the ideas and the potential impact
    * We are not adopting a CVPR-like model: we still have 5 reviews per paper, etc.
* Two tracks at SIGGRAPH; journal track is published in TOG. 
* Keep TOG high quality and integrated with SIGGRAPH
    * Journal track and straight-to-TOG papers presented at SIGGRAPH
    * Maintain timely reviewing process for TOG
    * Encourage revised journal versions of SIGGRAPH conference papers in TOG. Clarify and/or revise existing 30% rule-of-thumb.
* A subset of these proposals could also be adopted. For example, just imposing a page limit, and giving new instructions to authors and reviewers accordingly is an incremental change that could help a lot.

Other Notes
--------------------------

* SIGGRAPH isn’t going to balloon with submissions, but this will stanch the bleeding and reduce disincentives to submitting good work
* The main difficulty is explaining the nuances of the new system and expectations. But this has been done before, e.g., with the TOG transition, with different rules for rebuttals, and with the creation of SIGGRAPH Asia, etc.
* Should authors need to choose whether they're submitting to the conference or journal track at time of submission? I can see pros and cons; my inclination is to require authors to state at time of submission, to keep decision-making simpler. It could be useful to learn from the experience of other venues (like [IEEE VR](http://ieeevr.org/2019/), [ACM SAP](https://sap.acm.org/2020/), [IEEE ICCP](https://iccp2020.engr.wustl.edu/)) that have both conference and journal tracks, some with combined submission and some with separate submission.

**Discuss this on [Facebook](https://www.facebook.com/aaron.hertzmann/posts/10158397419855802) or [Twitter](https://twitter.com/AaronHertzmann/status/1259161919518150663?s=20).**

_This post benefited from online discussions with many people with many different viewpoints, including Keenan Crane, Alyosha Efros, Sylvain Paris, Olga Sorkine-Horning, Amir Vaxman, Etienne Vouga, and the commenters on the original Facebook post. I have made edits to this page after originally posting it, based on comments and feedback._
