# SIGGRAPH Conference Proposal

Following some recent discussions, here is a revised statement of why I think the SIGGRAPH Technical Papers program should add a conference paper track, rather than being journal-only. In short, **the requirements for publication at SIGGRAPH have slowly become overly burdensome since the switch to a journal-only format in 2003. This hurts authors (especially students), it makes it harder to publish risky ideas, and it's causing a brain drain as SIGGRAPH researchers move to publishing more in other venues.**

I originally [posted about this on Facebook last year](https://www.facebook.com/aaron.hertzmann/posts/10157508064645802); a [subsequent arXiv posting](https://arxiv.org/abs/1911.09197) provoked some discussions recently in private forums. This time I've put it in the form of a bulleted list. (See [the Facebook post](https://www.facebook.com/aaron.hertzmann/posts/10157508064645802) for more background on this discussion.)

The Problem: Expectation Creep
--------------------------

* **The expectations for publishing a SIGGRAPH paper have been steadily growing since the switch to a journal model in 2003, and they have become far too burdensome**
* Papers with good ideas get rejected because reviewers demand very extensive experiments and very highly polished results.
* Many of these extra experiments aren’t really necessary
* **Papers are getting longer and longer.**  Twenty years ago, the nominal page _limit_ was 8 pages. Anecdotally it seems like papers are now _averaging_ around 14 pages. This is an unnecessary burden on authors, reviewers, and readers. Some 16 page papers would have been better as 8 page papers.
* The second reviewing phase is an additional burden on authors and committee. The committee sometimes adds onerous, unnecessary requirements. 
* The high evaluation standards do not lead to papers with better ideas. 
	* There have always been plenty of SIGGRAPH papers that are "incremental" in their actual intellectual contribution, but this is not a bad thing
	* Risky papers are harder to publish because [convincing evaluation is more difficult for really new ideas](https://www.billbuxton.com/usabilityHarmful.pdf)
* It was easy to overlook these problems for a long time because SIGGRAPH had no real competition

Consequences: Brain Drain
--------------------------

* **Researchers are leaving SIGGRAPH when they can publish in vision**. Some of the most significant image synthesis work in the past several years are from SIGGRAPH researchers publishing at vision conferences.  Examples include [neural rerendering in the wild](https://moustafameshry.github.io/neural_rerendering_in_the_wild/), [NeRF](http://www.matthewtancik.com/nerf), [StyleGAN](https://github.com/NVlabs/stylegan), [pix2pix](https://phillipi.github.io/pix2pix/), [CycleGAN](https://junyanz.github.io/CycleGAN/), [Face2Face](http://www.niessnerlab.org/projects/thies2016face.html), and [PointNet](http://stanford.edu/~rqi/pointnet/).  
* Trend: SIGGRAPH will become a boutique venue for high-quality papers on geometry, physics, visual interaction, and a few other topics. As each of these topics become more intertwined with learning/vision techniques, they will migrate to the vision conferences, as has already been happening with rendering and geometry.
* While activity in adjacent communities is skyrocketing, e.g., vision, HCI, robotics, SIGGRAPH is flat. Flat isn’t bad, but it’s a warning sign.
* Not every paper has to be a journal paper
	* It's bad for students to only be able to publish one good idea a year in a highly-polished journal format, rather than being able to publish 2-3 good ideas a year in a reasonable conference format.
	* The vision and learning communities are making extremely fast progress in part because they have fast publication processes; things are changing very rapidly, and journal publication is increasingly rare.
* These other venues are not as good at fostering research where we care about output quality and usability

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

Other Notes
--------------------------

* SIGGRAPH isn’t going to balloon with submissions, but this will stanch the bleeding and reduce disincentives to submitting good work
* The main difficulty is explaining the nuances of the new system and expectations. But this has been done before, e.g., with the TOG transition, with different rules for rebuttals, and with the creation of SIGGRAPH Asia, etc.
* Another challengee is: How do you know whether to submit to conference or to journal track? There should be clear guidelines (e.g., level of polish and thoroughness of experiments, page length, etc). Note that there are other venues (like IEEE VR, ACM SAP) that have both conference and journal tracks. One could also have a combined submission process, though this could cause its own confusion.

**Discuss this on [Facebook](https://www.facebook.com/aaron.hertzmann/posts/10158397419855802) or [Twitter](https://twitter.com/AaronHertzmann/status/1259161919518150663?s=20).**


_This revision benefited from online discussions with many people with many different viewpoints, including Keenan Crane, Alyosha Efros, Sylvain Paris, Olga Sorkine-Horning, Amir Vaxman, Etienne Vouga, and the commenters on the original Facebook post._