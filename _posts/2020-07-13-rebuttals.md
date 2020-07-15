Technical Paper Rebuttals Aren't Just For "Factual Errors"
====================

This post concerns a very minor rule in the conference review process, but this rule speaks to basic questions of what it means to write a technical paper.

In many computer science conference review processes, including in graphics, computer vision, HCI, and others, there is a rebuttal phase, and often the instructions include a statement like ["The rebuttal is for addressing factual errors in the reviews and for answering specific questions posed by reviewers."](https://sa2020.siggraph.org/en/submissions/technical-papers) I think this rule, if taken strictly, is misguided and misleading. 

This statement probably came from an attempt to keep the review process manageable. SIGGRAPH has always shown a diligent focus on making the best decisions possible, to a degree that I have not seen in my experiences with other subfields, though this sometimes comes at the cost of being a lot of work. When SIGGRAPH introduced rebuttals (in 2003, I think), the rebuttal could be a PDF file with no restrictions—and some rebuttals were longer and had more experiments than the original papers! Clearly, unlimited rebuttals put a huge potential burden on both authors and committee members. In addition to restricting the length of the rebuttal, reducing the rebuttal's scope to factual errors must have seemed like a sensible way to limit the workload.  The HCI community copied SIGGRAPH's wording for UIST 2004, and later for CHI; this wording was still in place for UIST 2017, the last time I co-wrote a UIST rebuttal. The CVPR 2020 and ECCV 2020 instructions don't make firm rules, but they both indicate that the primary purpose of rebuttals is to respond to factual errors and reviewer questions.

What's the problem with this rule? It implies that bad reviews are bad solely because of factual errors. It implies that writing a technical paper is primarily about providing objective or factual information, and that the more subjective aspects of paper-writing aren't important. The first implication is obviously false, and the second one is more subtly wrong.

What is a paper?
=================
In a sense, most computer science papers have two components. The first are technical components: theory, algorithms, and experimental results. The second, however, is an _argument_ about why the technical components are significant. 

In most papers, the very specific algorithm presented isn't itself useful; it matters because of how it could be used in the future. No one cares about the experiments themselves for their own sakes. What we really care about is what we learn from these results, and whether it seems like these ideas will be useful in the future. Will this paper be influential? Will it lead to further developments in the field? Will practitioners want to adapt it to their own problems?

In short, reviewers and committee members should be judging papers according to the _expected benefit_ of publishing this paper: is this paper likely to be useful? (The potential harms should also be considered, such as from papers that with erroneous results.)

For some papers, the potential benefit is self-evident, and so little argument is needed. For example, a paper that get a clear improvement on an well-known benchmark using simple new ideas is likely to be a worthwhile paper. Conversely, a paper that gives a tiny improvement on a benchmark using a method that is baroque and unoriginal and difficult to use is unlikely to represent a truly valuable contribution.

But, in many cases, a paper proposes a different way of looking at a problem, or even proposes a new problem.  Sometimes the paper is really an argument for this new approach, and the technical components of the paper are really there to support that argument, showing a proof-of-concept for this new ideas. And sometimes papers simply develop ideas in an unpopular subfield. 

For example, I would say that most of my work in physics-based computer animation and computer vision falls in this category; physics in character animation research was once viewed very skeptically, and it still is in computer vision. Hence, each of these papers must explain why we believe physics could be useful in these areas, despite its many difficulties.

It is the authors' job to write the paper to convince the readers that these ideas could be useful. The authors need to connect the dots for the reader about why they should care. And papers are frequently rejected not because the technical components are wrong, but because the reviewers and committee members did not believe that the technical contributions had enough value.

What really happens?
===================

Consequently, rebuttals frequently do address non-factual issues. In one paper, our reviewers stated that the problem we proposed (image geolocation) was not a valid computer vision problem, appropriate for a computer vision conference. This is not a factual matter; our rebuttal argued for why this problem was worthwhile for a vision conference.  In one recent submission, reviewers said our paper should be rejected because we had unimpressive scores on a standard metric. This was factually true, but our rebuttal reiterated that the standard metric is misleading, and that there were other reasons to believe in the value of our contributions.

Most often, the art of writing a good rebuttal is not in identifying factual errors—this is the easy part and it's relatively rare that the reviewers' errors are starkly obvious. The art of writing a good rebuttal is in inferring the reviewers' belief systems from the haphazard comments they've dashed off, and inferring which issues are most important. And then, one must write to _persuade_.

One could argue that the authors should have gotten the argument right in the first place. But it's really impossible to predict all possible responses your paper. One writes using 
a mental model of the reader, based on the venue you're submitting to, and one writes the Introduction to persuade reviewers from this community. And yet, after I've been doing this for many many years, I still get blindsided by reviews expressing viewpoints that I never expected (sometimes these reviews make good points). But it's especially difficult when you're new to a field; in my recent submissions to perceptual psychology and art journals, I had no idea what reviewers would say to my submissions.

In reality, these rules that rebuttals are for factual responses are never followed. I have never seen any instructions given to reviewers to ignore non-factual discussion, and I've never seen anyone say "the authors make a good point, but I'm going to ignore it because it not a response to a factual error." In contrast, many reviewers and committee members at CVPR 2020 this year took seriously the new rule about not allowing new experiments in the rebuttal, because that rule addresses a real problem.

So the only real consequence of the "rebuttals are for factual corrections" rule is that it is unfair to researchers who are unfamiliar with the system. If you don't know how the game is played, you might think you're not allowed to write a persuasive rebuttal. This alone seems like reason enough to ditch this rule.