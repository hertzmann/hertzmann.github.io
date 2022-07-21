# SIGGRAPH Papers Committee Notes: 2022, and the future


So far, the new SIGGRAPH Conference Paper track that we introduced this year seems to be going well.   The technical papers chair Niloy Mitra and professional administrator Leona Caffey did an extraordinary job running the whole process. 

There were lots of difficult decisions involved, and hopefully future chairs will improve things and fix any policy mistakes that we made.

**In this post, I mainly want to discuss two difficult policy choices that will affect future SIGGRAPH Conference Tracks.**  This is particularly targeted to the PC members that are making these decisions, or anyone interested in the process. But first, some numbers and a bit about the meeting process itself.

**Some statistics.** We received 610 complete technical paper submissions: 257 for the journal track, and 353 dual track. 133 papers were accepted as journal papers, and 61 as conference papers. Out of the accepted journal papers, 17 of these had been submitted to the dual track as 7-page papers. In addition, 53 papers accepted directly to TOG and will be presented at the conference.

For comparison, SIGGRAPH 2021 received 449 full submissions and 149 were accepted for publication in the journal. The total acceptance rate was very similar: 34% last year versus 33% this year, but with a singificant growth in the number of papers, and the submission numbers support the idea that the new conference track was a big factor in this.

**Online committee meeting.**
As usual, the SIGGRAPH PC worked very hard to make the best possible decisions in the conference submissions. I really think that SIGGRAPH does better at this than the vision processes, and  [there's a lot they could learn from SIGGRAPH](/2021/03/03/ac-suggestions.html). Having plenary discussions is critical to people being able to learn from each other and shared decision-making. Currently the vision conferences aren't a single papers committee, it's more like 40 separate committees (or however many triplets there are), and the standards for vision reviewing are going to keep fracturing more and more.

**The SIGGRAPH PC meeting _the best large-scale, online, virtual meeting_ I have ever seen, by far. Other committees, including vision conferences, are hurting their communities by not having well-run virtual committee meetings.**  A big factor is simply having good software.

The virtual meeting tools, despite being home-grown, are so good that they actually have some real advantages over in-person meetings (but still some of the usual disadvantages). The information systems for SIGGRAPH are far, far superior to **the awful, dumpster-fire experience of using just Zoom+CMT+Gdocs for conference decision-making**. For SIGGRAPH, we have Linklings (Mark Montague), a highly-customized Ohyay space (set up by Kayvon Fatahalian), and Hepcat (by Adam Finkelstein).  There isn't any online description of these systems, but take a look at [Kayvon's description of his teaching on Ohyay](http://graphics.stanford.edu/~kayvonf/notes/virtualclassroom/) to get a sense of the customization possible, and then imagine specializing that to a PC meeting instead. One of us should really write a summary of how they work.

You don't know how bad you have it with online meeting systems until you try one that's run well.

# What is Conference vs. Journal?

This year, authors could submit either to the Journal Track, which operated like previous years (no page limit), or to a new Dual Track (7 page limit plus references). Submissions to the Dual Track could be accepted to either the conference or the journal.  This meant that the committee ultimately had to decide whether to accept a dual track submission to conference or to journal, which was often a difficult decision, and I think future chairs/committees should refine this further.  I'll describe here a rough sense of what I think it should be.

**The standards this year.** We told paper reviewers that all papers should meet SIGGRAPH’s high standards for papers with the potential to advance the research field and benefit the community, and that “The conference track is for new ideas with a clear (reproducible) algorithm, but ones that have not been exhaustively evaluated against a variety of alternative methods. Conference papers may be ‘riskier.’ For example, we’d accept any paper that presents an interesting idea/technique with the potential to make an impact, even if it does not have thorough experimentation. Indeed, riskier ideas are often harder to evaluate.”

As the papers committee went into the third day, I heard more and more of the committee discussions sound like "It seems like a journal paper has more experiments, and this paper doesn't have very many experiments, so we're going to accept it to the conference."

**Counterexamples.** I don't think that experimental rigor should be the sole standard for conference vs. journal. Here's one SIGGRAPH 2022 journal paper that doesn't have very many experiments: **[Towards Practical Physical-Optics Rendering
](https://ssteinberg.xyz/2022/04/03/practical_plt/).**  It's 24 pages long, so it must have been a journal-track submission. It seems like a good example of a journal paper that deserves to be published in a journal, despite not having "extensive experimentation."  

I'm sure there are many other examples in TOG's history, but one that I'm familiar with is our [TOG 2014 paper on occluding contours](https://www.labri.fr/perso/pbenard/publications/contours/).  The paper also doesn't have very thorough experiments, but it's 20 pages long nonetheless, and I don't recall any reviewers complaining about the thoroughness of the experiments.


**A bit of history.** 
Here's a little bit of historical context. In the 20th century, peer-reviewed journal papers (and books) have historically been the main outlets for scientific and scholarly work. This persists in many fields, where conferences are mainly for preliminary dissemination and feedback. In many fields, conferences accept 80+% of submissions without peer review, based on the abstract and authorship alone. Journal papers are meant to be thorough, carefully-written, and complete pieces of scholarship; "archival" pieces of knowledge to be stored in the library and available for future generations to reference.

As I understand it (thanks, Moshe Vardi), computer science started out the same way. But then conferences became more selective, and then they started to add peer review, and conferences published full papers.  In [Jim Kajiya's talk from around SIGGRAPH 93](https://www.ee.columbia.edu/~sfchang/course/svia-F03/papers/siggraph-reject-how.htm), he wrote that the principal feature that made SIGGRAPH attractive was "speed. SIGGRAPH is one of the few high-quality publications that can publish a paper in less than a year. In 10 weeks, SIGGRAPH can do what other major publications take 10 months to do. In a fast-moving field like computer graphics, this is crucial."

All the papers from my PhD (2001) were published in conferences, and that was enough to get a faculty position. When I published my first first-author computer vision paper (CVPR 2003), my coauthor/mentor Steve Seitz told me we should really submit to a vision journal. We extended the algorithm, added new experiments, and revised the text to address feedback from CVPR and elsewhere. [Our PAMI 2005 paper](http://grail.cs.washington.edu/projects/sam/) is the authoritative version of this work and there's no reason to read the CVPR version anymore. 

When I went up for tenure, I was told it was good to highlight journal papers on my CV. I received several interdisciplinary awards where having journal papers on my CV was important, since my CV would be compared with people from, say, math and physics.

Ten years later, new transformations began. People started talking about [radical changes to publishing models.](http://yann.lecun.com/ex/pamphlets/publishing-models.html) Since the start of the ICLR conference, arXiv preprints have become widespread, along with experiments like [distill.pub](https://distill.pub/), and [TMLR](https://www.jmlr.org/tmlr/). Within the graphics community we hear opinions that range from "arXiv preprints shouldn't be allowed; everything should be strictly [dual-anonymous](https://www.acm.org/diversity-inclusion/words-matter) peer reviewed" to "academic publishing as we knew it is over, we should just post to arXiv and let social media sort out the best work." I'm very curious to see how things go with [TMLR](https://www.jmlr.org/tmlr/); that process seems very appealing.

For the moment, I believe there's value in many different kinds of publishing; there's value in conference papers, in journal papers, in arXiv, in social media, and we shouldn't try to shoehorn all publication into one format.

**What should it be at SIGGRAPH?**  
A journal paper is a complete, archival piece of scholarly, scientific, and/or technical research.  A conference paper contains most of the material of a journal paper, but may be missing some important experiments or theory. It might be "riskier", it might be missing some of the experiments that a full journal paper should have.

(All of these terms are subjective and ambiguous, this is normal for calls-for-papers; most explanations of what kinds of papers a conference or journal accepts has similarly subjective terms like "high-quality" and "impact." It's impossible to put any of these standards in precise, concrete terms.)

In most cases at SIGGRAPH, the difference is whether the experimentation is thorough. **But journal vs. conferences isn't _always_ about the level of experimentation.** For example, the examples I listed above ([1](https://ssteinberg.xyz/2022/04/03/practical_plt),[2](https://www.labri.fr/perso/pbenard/publications/contours/)) don't have extensive experimentation in my opinion, but they do have extensive theory, math and/or theorems.

**Are there other examples of different _kinds_ of journal papers that have been published at TOG** that could help define this precent? I think the standard for "journal paper" should be anything that is somehow "complete" and rigorous, but it would be nice to have specific examples of what that has meant in the past.

In other disciplines, journal papers could be many things. I've seen math journal papers that present a theorem in two pages total. Many journal publish "review" papers and papers that express an opinion about the field.  I really liked the NPAR meta papers track and I think more of our venues should offer tracks for publishing reviews, opinions, visions for the field, and so on.  Some of my favorite papers were essentially position papers, and many of our conferences have no venue for such papers.

(By the way, anyone who wants to publish a survey/tutorial paper should contact me about submitting to [Foundations and Trends in Computer Graphics and Vision](https://www.nowpublishers.com/CGV)).



# Preventing Expectation Creep

For me, [the main goal of adding the conference process to SIGGRAPH is to reduce workload on paper authors and reviewers](/2020/05/08/siggraph-as-conference.html) compared to the existing journal process. Starting with the first SIGGRAPH in 1974, all papers were published in conference proceedings. In 2003, all subsequent SIGGRAPH publications were published as journal papers, and, with the end of printed proceedings in 2013, [the page lengths for SIGGRAPH papers grew longer and longer](https://twitter.com/_AlecJacobson/status/1259526238378561536), with common stories of papers going through many rounds of resubmission with reviewers asking for more and more experiments and changes.  The amount of work required to author and to review each paper grew considerably, and many graphics researchers started publishing their papers in vision conferences instead (myself included).

The goal of the conference track was to draw the brakes a bit: with a 7-page limit, and explicit understanding that conference papers can be less thorough than journal papers, hopefully this would save everyone time and effort and make submitting more appealing.

However, in the PC meeting this year I heard a strong urge to add flexibility to the process in ways that, ultimately, could make things worse again. Flexibility is how we got into this mess in the first place. 

Flexibility causes Expectation Creep: the more wiggle room there is in the process, the more that authors will need to do more work to succeed, and the more work this creates for committee members. Some flexibility is good and helps everyone, but too much ends up being harmful.  It's good to have rebuttals, but they need to be limited. They should be sensible limits, not like that vision conference that limited the number of characters in the rebuttal; I remember seeing my colleague removing most of the vowels from his rebuttal. Finding the right trade-off is hard.

The main example that springs to mind is whether or not PC members can impose new experiments in the Required Changes onto Conference Papers.


**Flexibililty considered harmful.**
One of the wonderful things about the SIGGRAPH PC is the degree to which people take the process seriously and want to help each other and the authors. But it can go too far.  Here are a few examples where the trade-off can be a fine balance.

The purpose of **Required Changes** is to allow authors to add writing/experiments that, without which, the paper can't be accepted. This allows papers to be accepted that would have been rejected. But, occasionally journal required changes veer into the territory of long lists of experiments that would be "nice to have."" I have my own share of papers like this (I'm looking at you, Eurographics).

The addition of **rebuttals** to the SIGGRAPH review process made the process more flexible by allowing authors to respond to problems in the reviews. (I think SIGGRAPH was the first—or one of the first—conferences to allow rebuttals.)  But the process can be too flexible. IIRC the first year, rebuttals could be unlimited-length PDF files, and one paper had a 60-page PDF rebuttal with figures. This is too much, for both authors and reviewers. There was also an author BBS for discussion with authors, which was really bad too. I've heard similar things when ICLR later tried the same thing, they had the same problems: authors felt like they were on call during the rebuttal week, trying to answer every BBS comment and request for new experiments during the week.

Having **dual-track submissions**  that can be considered for both conference and journal acceptance makes it more likely that these submissions will be accepted to the best-fitting track, and not be rejected; it removes stressful guesswork from the authors deciding where to submit (especially in the first year, when the difference is unclear). But it creates more work for reviewers and committee members. Maybe in the future the tracks can be separated to save reviewer time/effort.

Most large conferences I know (including SIGGRAPH) do not allow **extensions or late submissions**. But suppose you are organizing a small workshop which receives 10-20 submissions and authors ask for an extension. It's reasonable to grant an extension, as long as you announce it publicly and early enough.  Now suppose you are organizing a conference with 1000 submissions.  Handling late submissions creates huge logistical problems in an already complicated, stressful process, as well as a big fairness problem. (It's the same thing if you are teaching a class of 10 students and allow extensions, versus teaching a class of 100 students.)



**Questions that came up this year:** At the IPC meeting, I heard PC members ask for:
* The ability to require new experiments in conference acceptances.
* The ability to add more pages to conference acceptances.

They said this flexibility will allow us "to accept more papers." Which is true, and a fair point.  My fear is that, the more of this flexibility we allow, the more temptation there is for reviewers/PC members to add more and more requirements for each acceptance, to put undue requirements on authors. Are all these "requirements" really necessary?  

Sometimes it feels like Required Changes aren't about what's _necessary_ for the paper, but they're compromise tokens for PC members that are struggling to decide whether the paper is interesting enough for acceptance. Somehow adding Required Changes makes it easier to accept a paper that you're uncertain of the significance of, even if the new experiments do not  make the paper more or less significant.

For all committee members, if you are saying "I would love to accept this paper but it is missing X", ask yourself if X is really, genuinely necessary that it should be a requirement. In some cases, the answer will be yes, but I suspect not always.

Why have Required Changes for conference papers at all?
At the outset of the process, I originally advocated for not having Required Changes  for conference papers _at all_. Papers would be either accepted or rejected, and the committee should accept the fact that some papers will be accepted with unsatisfying issues. This is the way conference acceptances have always worked, and it has largely worked out. Very few other conferences today have Required Changes.  

When I had my first paper accepted, to SIGGRAPH 98, my advisor said I should try to do the things the reviewers asked for, even though no one would check and I could make whatever changes I wanted to the final paper. In principle, with most conferences, you could replace every word in the final version with "chicken", and no one would check. But people don't do this (unless [the submission was like that](https://isotropic.org/papers/chicken.pdf)).  

I currently do think that Required Changes should be allowed for writing, but not for experiments. People do occasionally complain that authors did or didn't cite previous work properly in final versions, which can be fixed with Required Changes to writing.

Allowing required experiments and adding pages points us toward the slippery slope of more and more requirements each year, which is what got us into this mess with journal papers in the first place.
