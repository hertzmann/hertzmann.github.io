---
layout: page
title: Suggestions for Computer Vision Review Processes
summary: Some ideas to improve the CVPR/ICCV/ECCV AC-ing
author:  AaronHertzmann
image: /images/cvpr-abe.jpg
---


# Suggestions for Computer Vision Review Processes


I've been complaining for years ([2018](https://www.facebook.com/aaron.hertzmann/posts/10156213809160802), [2019](https://www.facebook.com/aaron.hertzmann/posts/10157112098565802), [2021](https://www.facebook.com/aaron.hertzmann/posts/10159234214220802)) about certain aspects of the reviewing processes at the top computer vision conferences (CVPR, ICCV, and ECCV), and now I guess it's time to write out some more concrete suggestions.

I don't have one single set of suggestions; there's no one right way to do things anyway. Besides, a lot will hinge on whether we have in-person or virtual meetings (though I have a lot to say on this topic too). Instead, here are a lot of ideas and observations that could be useful for improving the processes.

**But first,** I want to acknowledge that running these processes sounds extremely demanding and I've never done it, especially given the _literally_ exponential growth in numbers of submissions. So all due respect to the volunteers who put so much effort into this process, sometimes multiple years in a row. 

One benefit of being on the committee (especially when it's in-person) is seeing how much hard work the other ACs and the chairs put into it, and how seriously they take the process. People really care about making it work and doing a good job. I've heard lots of people who just finished their first AC meeting say that it made them feel much better about the review process than before. No process is perfect, but people do a good job.


[Some further discussion on this post is here.](https://www.facebook.com/aaron.hertzmann/posts/10159244322970802)

**Update: I'd summarize the biggest problems  as:**
* Review process puts most of the weight on the reviewers, with few checks or balances
* Little or no training for ACs, or consistency between them
* Paper matching algorithms don't work well

**Maybe these problems are hard to fix, but there are lots of reasons to believe that it's possible to do better.**
I don't mean to imply that SIGGRAPH is doing better than the vision conferences; that's [very obviously not true](/2020/08/31/cvpr-graphics.html).** But I think there are things each conference can learn from the other ones.

<center>
<figure>
  <img src="../../../images/cvpr-abe.jpg" alt="Old Man Yells At CVPR graphic"/>
  <figcaption align="center"><i><small>Mash-up by Rich Radke</small></i></figcaption>
</figure>
</center>


The State of Things at CVPR
=======

**I interpret the CVPR committee philosophy as, roughly: the three reviewers select the papers, and the ACs (Area Chairs) manage the process and break ties in difficult cases.**If the reviewers reach a consensus, then the AC is not explicitly expected to read the paper. In more difficult cases, the AC often cannot get help outside of their triplet, even in difficult cases, or where the reviews are all borderline and the ACs do not know the subject area well. When the reviewers make a unanimous accept decision, going againt this decision is called "overturning" the reviewers, as if they were an judicial tribunal, no matter how slapdash the reviews actually were.
 
Putting so much weight on the reviewers is a mistake. Even the most knowledgeable reviewers may have difficulty evaluating some work. Maybe they didn't invest much time in the review, or think very carefully. Maybe they missed something.  Maybe they weren't very knowledgeable, or they weren't very experienced. And the reviewers don't have the same responsibility and investment in the decisionmaking that the ACs have. It's easy to form strong opinions when you're just checking a box on an online form.

Likewise, it's a mistake to engage many of the most experienced experts in computer vision to form a paper committee, and then squander most of their expertise during the decisionmaking process. As an AC, if you are assigned a paper in an area that you are not expert in, and the other ACs in your triplet are also not expert, or else you just need another opinion, it is nearly impossible to consult with any other ACs on the committee for help. (It used to be slightly easier when there were "panels," but these would still have the snap judgement problem, described below.)

 


_Note: At the vision conferences, each year, the papers chairs are actually free to run the process pretty much however they want. In theory, next year's chairs could decide to replace the entire papers committee with an angry monkey. However, it's been years since there were papers chairs that really went off the rails._


The SIGGRAPH Process in a Nutshell
===

In contrast, I like the SIGGRAPH ethos much better, which seems to be **the ACs are responsible for making the best possible decision for each paper, using all resources available in a limited time budget.** The process has numerous steps aimed at getting better matches between papers and ACs, getting ACs the help they need to make good decisions, and mitigating some of the cognitive biases that can lead to bad decisions. 
(At SIGGRAPH, the terminology is "papers committee member," but I'll use the term AC for simplicity.) 

At SIGGRAPH, each paper has a primary AC and a secondary AC, and together they assign 3 reviewers.  Both ACs write full paper reviews, so each paper gets 5 reviews. After a discussion period, the ACs may ask for help from any other unconflicted AC. That "tertiary AC" then reads the paper and writes a full review. The three ACs then discuss the paper and make a decision. One or two more ACs can be added, e.g., if multiple kinds of expertise are required. (Note: it's been a few years since I've been a SIGGRAPH AC and I might be a little out-of-date.)

As a whole, this model would not scale to CVPR's volume. But it is worth recognizing several benefits:

* ACs are assigned based purely on topic matching, without conflict constraints from buddies, triplets, or panels. Each paper can expect to be evaluated by the ACs best suited to do so.
* Each AC has read their papers in sufficient detail to write a full review
* Multiple experts discuss each submission to come to a decision. 
* Each AC—including tertiaries—has read the paper at least a week before the final discussion, allowing them time to ponder and "sleep on" their evaluations. This fixes a problem where, in previous years, there have been problems with tertiary ACs making snap decisions based on their first impressions of a paper.  (This is a surprisingly easy cognitive trap to fall into, and I'm sure I've fallen into it in the past.)

Perhaps some of these ideas or goals could be incorporated into the vision processes, even if just a little bit.

Sometimes [SIGGRAPH goes overboard about being "too dilligent" in making decisions in ways that are harmful](/2020/05/08/siggraph-as-conference.html), whereas the vision conferences goes overboard in not investing nearly enough in making decisions.  Fortunately, SIGGRAPH has corrected for some of the biggest past mistakes, such as the original rebuttal system (when authors could upload an arbitrary PDF rebuttal, and boy did they), and papers being discussed by ten or more ACs at the meeting.


One concrete proposal: Tertiary ACs
====

Here's a concrete proposal for a modification to the vision process that uses some of these ideas.

ACs are paired into buddies, and each submission has a primary AC and a secondary AC who are buddies.  Papers that have a clear consensus after the rebuttal can be accepted or rejected, as long as the primary AC is comfortable with the decision. For each remaining paper, the primary AC has the option of requesting a tertiary AC; this tertiary AC can be any AC that is unconflicted with the paper (and not overburdened with requests). They should do this for every paper for which the primary and secondary are not sufficiently expert on this topic to make a confident decision. 

The tertiary AC will read the paper _prior_ to the committee meeting. This guarantees that each difficult case has one AC that has read the paper and thought about it well before the actual AC meeting.  Ideally, the tertiary reviewer would also write a full paper review, and they would do this before having access to the other reviews or the paper discussion.

Then, during the committee meeting, the primary and tertiary will get together to make a decision on the paper. Involving the secondary AC is optional (e.g., if the secondary doesn't feel like they can contribute).  For papers where no tertiary is involved, the primary and secondary can discuss the paper between themselves. So, as compared to previous buddy processes, some of the time at the committee meeting (assuming in-person meetings) means finding time to meet with your tertiaries to finalize decisions on a few difficult cases. For a week-long virtual AC meeting, this means scheduling ad hoc meetings during the week.

_This proposal is based on a discussion with Bryan Russell._


Less Time For Oral/Poster Decisions
=========

The above proposal does require some more effort than now. **We can free up some time for discussions by using both days of the two-day AC meeting for acceptance decisions**. 

In every in-person vision AC meeting I've been to (my first was in 2008), the first day is spent on accept/reject decisions, and the second day is spent on oral/poster ranking.  This seems really imbalanced to me; obviously, the accept/reject decision is much, much, much more important than oral/poster. 

Once you've made the accept/reject decisions, the oral ranking is relatively straightforward; you just need some group discussion for calibration, and there's no benefit in agonizing over a ranking that might later be adjusted by the chairs based on capacity. I chaired one oral/poster ranking group last year. We were done in ninety minutes, and I think we did a perfectly good job at it.


Of course, like a lot of these choices, the specifics hinge on whether we have in-person AC meetings at all, since we may be rethinking some of these things after the COVID experience. For CVPR 2021, we spent very little time on oral/poster, since the conference is virtual anyway, and we were given explicit instructions not to overthink it.



The Plenary, Socialization, Training, and Community Standards
====

At SIGGRAPH, all decisions other than clear rejects are discussed in a plenary meeting. At times the plenary might seem tedious and inefficient. But **I think the plenary serves several vital roles for the community, which are missing at the vision conferences.** There may be some other way to replace them, but, right now, these needs are not being met.

When each paper is brought up in the plenary, the entire papers committee is in the room, except for people with conflicts of interest. The primary stands up and briefly describes the paper, the decision, and the reason for the decision. If the decision is difficult, then the primary describes why, and a discussion may follow in the larger group.

This plenary meeting serves a crucial role of making difficult decisions in a larger group, and sharing the reasoning for these decisions. There are always difficult cases, and the difficulties change from year to year. Here are a few examples of things I've heard discussed in the SIGGRAPH plenary (all of these examples are over 10 years old, or are composites):

* A reviewer pointed out a "published patent application" on the USPTO website that proposes the same idea as the submission. Do we still accept the paper?

* Some reviewers are excited about the paper because the idea is clever and delightful, but others say that the method is completely useless and doesn't solve a real problem. Should we accept the paper?

* People mostly like the paper, but there are concerns that the paper is sexist. Is it? How does this affect the decision? Are there instructions that can be given to the authors to address these concerns?

Having this shared decision-making process has many benefits:
* **Difficult "policy-like" decisions are made together, than by individual ACs acting alone.**  
* **Consistent standards evolve.** As these decisions are communicated, they can be used to inform other decisions in the room, instead of having inconsistent rules be applied to different papers.
* **New committee members learn how to make decisions.** This is especially important for junior members for the committee to learn how the process works, as well as members from other fields. But it's also helpful for keeping senior members calibrated as things change over time.
* **You learn how other subareas make decisions.** For example, I don't work in physical simulation, but it's helpful to me to hear what things the simulation experts think are important or not important.

Compare this to the vision conferences, where all decisions happen in triplets. In rare exceptions, the only other ACs you ever talk to are the two other members of your triplets. I've heard of triplets where are three ACs were first-time committee members, and the triplet had no senior mentorship. How did they decide difficult cases?  By nature, triplets are also necessary imbalanced in their biases: this year, both members of my triplet work at the same company as me, and one of them is a frequent collaborator. I've also heard of Google-only triplets.

In vision, there are numerous difficult cases that should be discussed by a larger group. How are diffcult ethical questions handled?  When do we accept a paper has good incremental benchmark scores but seems technically weak? [What kinds of computer graphics papers should be accepted?](/2020/08/31/cvpr-graphics.html) In fact, as I was writing this I found out that had a paper rejected for CVPR 2021 on the basis that it was a computer graphics paper, whereas my collaborator had her paper accepted in almost the exact same subarea of graphics. The lack of a group decisionmaking process means that different ACs can be applying wildly different standards, year after year, without even realizing it.

**Options**. I don't have a solid suggestion here; given the massive scale of submissions, directly adopting the plenary format is impossible. I don't think there's any way to do this that doesn't require more work. However, I think that this is an important problem for chairs to think about. How do we create a sense of shared standards for the community?  

Here are two ideas:

* We really only need plenary discussion for a small subset of hard cases. A plenary for group discussion of a selected set of hard cases. Perhaps ACs nominate papers for group discussion that seem to involve some sort of hard "policy-like" decision. However, there may not be enough time for an in-depth discussion, but the discussion may reveal just how deep the divisions are between different approaches to ACing. 

* The vision conferences used to have a notion of *panels*, in which the papers committee was essentially divided into four conflict-free subcommittees. These could somewhat play the role of the plenary, although they still don't share information between panels. 


Virtual vs. In-Person
=====

For years, people have been complaining about in-person meetings for various reasons, including the environmental cost and inclusion. Conferences have experimented with virtual AC meetings on-and-off for years; this year's Zoom virtual triplets felt very similar to the Skype virtual triplet format at the ECCV 2012 AC meeting. Likewise, we have just spent the past year doing an unplanned experiment in having all meetings go virtual. So far, I think all of these virtual formats fall far short of the benefits of in-person meetings, sometimes in ways that are not obvious.

The criticisms of in-person travel are completely valid, but they don't seem to come with an acknowledgement of all the benefits of in-person meetings. **If more processes are to go virtual, then we need software and workflows that can compensate for what's lost. And there are many non-obvious things that are lost.** I get the impression that people don't recognize all the many benefits of in-person meetings. 

There are some obvious benefits of in-person meetings. It's just harder to communicate and make decisions over video calls, especially with someone you don't know. Decisions tend to be more extreme over the phone (I think I've seen old studies that confirm both these points). There's no real opportunity to build connections with people in the community, and simply to meet people face-to-face, which is very important for many reasons. We are social beings, and both community and good decisionmaking depends on our social connections.

But I think there are other, more subtle things that are lost in in-person meetings as well. The socialization and plenary are the most significant of these. It's hard for junior people to meet people, and learn how things work, and to get incorporated into the community. It's harder to renew the personal connections, and find consensus. 
And, **until our software tools and meeting formats can address these issues, virtual meetings can cause long-term harm to the community.**  Tools like Gather, Ohyay, and Spatial are making incremental steps toward capturing some of these benefits, but they have a long way to go.




Submission and Review Systems
======

At the scale of CVPR's thousands and thousands of submissions, having submission systems with **good user interfaces and workflows** is crucial. Building effective interfaces and workflows is very very hard. But creating good conference management systems has generally been an afterthought; no one wants to work on them, or to listen to users' needs, or to iterate and improve the systems.  Building new information systems is beyond what papers chairs can reasonably handle, and I suggest that **the Computer Vision Foundation (CVF) invest in building new infrastructure outside of any specific conference.** This new system should be made with the users in mind, and it should be reconfigurable and modifiable as processes change and new needs are identified.


Many workflows in CMT require many unnecessary steps, and data visualization is frequently quite difficult. The problem isn't that CMT is badly-built (I have no idea), it's that these systems need continual update based on user needs. Any HCI or UX expert will tell you that you can't build an interface based just on a list of user requirements, you need to iterate with actual users. And, since conference processes keep changing every year, you need the ability to change the system to go with it. Perhaps even professional staff to support the chairs in updating the system. Instead, CVPR has been using a mishmash of CMT and Google Docs to manage processes, plus who knows whatever bespoke coding the conference chairs are doing.  (I haven't used OpenReview as an AC, so I can't comment on it).

SIGGRAPH, after going through many different systems, each with their own problems, has recently settled on a submission review system built by Linklings, and, personally, I think the Linklings system is by far the best conference review system I've used.

Paper matching
=====

I suspect that all vision ACs can agree with the following statement: **The single thing that would most improve the reviewing process is to improve on TPMS**. The [Toronto Paper Matching System (TPMS)](http://torontopapermatching.org/webapp/profileBrowser/about_us/) was an innovative and forward-looking system created by Laurent Charlin and Rich Zemel in 2010. It's been widely used since then, long after Laurent finished his PhD, and I don't get the impression that it's been substantially updated since. While [the published paper](http://www.cs.toronto.edu/~lcharlin/papers/tpms.pdf) doesn't describe the precise details of the deployed system, TPMS defines the affinity between a submission and a reviewer as the dot product between the word histogram in the submission and the word histogram across all of the reviewer's papers (plus some additional topic modeling and a mechanism for handling the cold start problem). In other words, if your published paper has the exact same distribution of words as the submission (no more and no fewer), you're more likely to get assigned that paper for review.  There are some model parameters, and it seems like CVPR 2021 might still be using parameters trained on data from NIPS 2010.

Anyone who has used TPMS at CVPR has seen that it's better than the heuristics in CMT, but it is still poor in both precision and recall. That is, it often makes some good suggestions, but often the best choice is someone pages down in the list.  And this matters: assigning reviewers is hard work, it's the most important part of the review process, and it's very difficult even to know who to ask. At the scale of CVPR, these kinds of search algorithms make the difference between finding the best reviewers and not.

A familiar sight in the review assignment process is to see that some specific grad student appears high in the list of recommended reviewers for nearly every paper you check. This grad student has only published only two or three papers, whereas very experienced authors who have published many papers related to the submission topic are much lower in the list. Indeed, in the TPMS bag-of-words affinity model that I summarized above, an author who has a wide range of publishing experience is a worse reviewer than an author who has published one paper on the topic of the submission. No other cues are used explicitly, e.g., overlap in which papers are cited.

This leads to a real problem:  that grad student who has only published two papers but appears at the top of the recommendation lists? ACs have suggested them as a reviewer for 90+ papers!  Clearly, some ACs are blindly following TPMS and not using their brains or doing their jobs when doing review assignment.  Or maybe they are overworked and undersupported by the information systems.

There's a big problem in training a TPMS successor. Where do you get supervised data for training the system? While CMT and OpenReview ought to have lots of good data, review assignments must be confidential, and there's no effective way to anonymize them for outside researchers to work with.  

Note that modeling this data would require which review suggestions were shown to ACs, e.g., an AC is more likely to assign a reviewer when they have a high TPMS score, indendent of all other factors. In this way, modeling this data bears resemblance to [implicit feedback models used in training search engines](https://dl.acm.org/doi/abs/10.1145/775047.775067).




Meta-Point: On the Need for Change and Cross-Fertilization
========

It's easy to lose sight of the possibility of alternative conference processes.

The first time I visited a foreign country, I think I was surprised most by [the little things](https://www.youtube.com/watch?v=6Pkq_eBHXJ4). Little assumptions that I hadn't realized. Like the fact that you don't need to tip in restaurants. I suspect most Americans would assume that restaurants could not function without tipping, and would reflexively list several reasons why obviously you need tipping, and abolishing tipping would ruin everything. Then you travel to foreign countries and it becomes clear how wrong this is. The same can be said for typical received American attitudes toward many other things like public transportation and universal health care.  

Similarly, when I first started ACing at vision conferences almost twenty years ago, I was shocked that they did things differently from SIGGRAPH.  It wasn't that the vision processes seemed wrong—it was just that it hadn't occurred to me that there was anything different from the SIGGRAPH way.

In general, since most of the members of these communities only publish in their own field (just like [most Americans don't travel outside North America](https://www.forbes.com/sites/lealane/2019/05/02/percentage-of-americans-who-never-traveled-beyond-the-state-where-they-were-born-a-surprise)), there is a built-in conservativism, a lack of awareness that other kinds of review processes are actually possible and might even have advantages.

Over the years, there's been a little cross-fertilization. As far as I know, the concept of rebuttals began at SIGGRAPH, and then spread to many other conferences, including vision (I'm not 100% sure about that though). Likewise, following the vision and learning conferences, this year SIGGRAPH conference chair Sylvain Paris made the rules explicit that arXiv posting was allowed. 

There are some really good things about the SIGGRAPH review process, but there are also ways in which [it is stuck in a bad local minimum](/2020/05/08/siggraph-as-conference.html). Likewise, I think the vision conferences have many good things, but they are stuck in a local minimum as well; they have been converging to a particular review process that I don't think serves the community very efficiently. In part this is the product of exponential growth in the number of submissions; the conference chairs have understandably trying to figure out how to scale the process, and just dealing with this is no doubt itself a major challenge.

But I think it's worthwhile to take a step back and think about where the process has arrived and if there are good jumps to make outside of this local minimum. And learning from the experience of other conferences is a good way to do it.

(I've never AC'd in other fields, but there might be good ideas in other places. For example, UIST has an interesting multi-stage process that seems to have some advantages and disadvantages. There have been a lot of interesting experiments happening in the machine learning conferences in the past decade. Now that there are several years of experience with ICLR's open reviewing experiment, it would be hear to learn about how that has gone.)

