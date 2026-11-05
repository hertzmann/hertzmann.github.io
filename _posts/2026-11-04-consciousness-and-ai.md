---
layout: post
title: "Conscious AI is Profoundly Unlikely"
description: "We will not make conscious machines in the near future."
date: 2026-11-04
image: "/images/brains/calculator.jpg"
tags: [minds]
---


Here I explain why I think it's profoundly unlikely that our AI algorithms will be conscious in the foreseeable future, and why I think you should too. We should not take the idea seriously enough to let it influence our choices, or public discussions about AI.

To reason about real-world AI consciousness, we need to consider both the theoretical question of whether an algorithm could ever be conscious, and also the _practical_ possibilities of software that we could run on modern or near-future computers. Our modern understanding about real software systems should not be driven by [science fiction scenarios](/2026/08/05/science-fiction-ai.html).

To make this case, I will consider what we know about biological consciousness and discuss how different it is from computing. Then I will discuss serious limitations of some of the arguments for computer consciousness.  There are a range of possibilities for the nature of consciousness, and I will ultimately argue that conscious AI is highly implausible across all of them.  

This post is aimed at many of the commonplace arguments I hear for AI consciousness, but it's inspired by ideas from philosophers and neuroscientists that I have found persuasive. See the end of this post for philosophical references and jargon. I'm grateful to Rosa Cao for many conversations on this topic that influenced my understanding and thinking (although all the mistakes are my own).


# Ways to reason about consciousness

Reasoning about consciousness is notoriously tricky. 

People often point that difficulty as itself a sufficient reason to take AI consciousness seriously. "You cannot prove that you are conscious!", they say, or ["We don't know what consciousness is."](https://www.nytimes.com/2026/11/01/opinion/ai-consciousness-ethics.html) If you don't know what it is, then maybe AI has it?

This kind of skepticism could justify almost any belief. But most of our knowledge in life does not come from scientific tests. 

And, we can actually say quite a lot of useful things about consciousness.

**First, you know that you are conscious**, because you have your own awarenesses, experiences and feelings. 

**Second, you can know that other people are conscious**. This is called ["the problem of other minds"](https://plato.stanford.edu/entries/other-minds/) in philosophy, and has been discussed for over a century. In brief, you know that other people have the same basic biology as you, and the same broad kinds of behaviors, many of which go together with consciousness (like describing their feelings or experiences). Given all your direct experience and knowledge, it makes much more sense for you to think that other people are conscious than that they are all pretending. I've written about this more [in a previous blog post](/2026/05/20/consciousness.html).

**Likewise, animals share enough of our biology and behaviors** that we can be confident that many kinds of animals have some form of consciousness. We also know that their consciousness must be different from ours in important ways. This is also discussed [in that blog post](/2026/05/20/consciousness.html).

**Now, just observing behaviors alone is not enough.** We are easily fooled. Even [simple chatbots like ELIZA](https://en.wikipedia.org/wiki/ELIZA_effect) have fooled people into thinking that they're human since the 1960s. And I'm sure we could be convinced that puppets were really alive if we did not know about puppeteers.  Moreover, chatbots, like ELIZA and ChatGPT, are engineered specifically to mimic human behavior.

**Finally, I think that most of us would take as our default assumption that _most things are not conscious_.** If you fervently argued that a rock or a chair or a refrigerator were conscious, most people would think you either unserious or mad. The invention of a new, conscious technology would be a truly extraordinary, unprecedented development in human history.

So there is a lot that we can say about consciousness, even without having a scientific test for it. **To determine if something is conscious, and what that consciousness is like, we compare both its behaviors and mechanisms to our own. Moreover, our default assumption for things is that they are not conscious.** Each of these statements raises difficult questions, like "_how_ should the mechanisms be similar?"

We know that computers can mimic some human behaviors well (chatbots). Hence, whether computers can be conscious primarily comes down to the question of whether human consciousness is a product of computation and _nothing but_ computation. If so, can that computation be practically implemented efficiently within the foreseeable future?

So let's look at the mechanisms: what we know about how the brain works, where consciousness might emerge, how that relates to computing, and then some of the practicalities.


<center>
	<figure>
		<iframe width="560" height="315" src="https://www.youtube.com/embed/LOBn86_DAZU?si=_E2zuqvzUA4ctkE8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
		<figcaption><i>For judging consciousness, behaviors are not enough. When watching a skilled puppeteer, you sometimes have to remind yourself that the puppet is not actually alive.</i></figcaption>
	</figure>
</center>



# Biological brains and digital computers

Let's next review the biology of human brains, along with the logical foundations of computing.  Since we do not know what consciousness is or where it comes from, we have to consider brains as a whole, consider which aspects might be necessary for consciousness, and which of those are shared by computers. 

Often I hear the claim from colleagues that "the brain is just a computer." [I've written previously ](/2026/07/13/brain-not-a-computer.html) about how different brains and computers are, and why we cannot effectively simulate a brain in a computer. I'll review a few key points here, since this is important.

On one hand, our **modern digital computers are logic machines**: manufactured objects that perform binary logical operations, and interface to the world with various sensors and displays. Quantities are encoded as variables, variables are encoded as strings of bits, and bits are encoded as voltages in electrical circuits.  Likewise, computer operations go through corresponding abstractions: all high-level computer software is converted to logical operations on bit representations. Simulating a fluid flow or a neural network is always reduced to binary logical operations.

On the other hand, **human brains are parts of biological organisms.** Brains operate through the functioning of biological cells called neurons, and each neuron is a highly complex nonlinear system. An average neuron has 7000 dendrites, which are strands that receive communications from other neurons, but [each dendrite has its own memory state and nonlinear dynamics](https://www.thetransmitter.org/memory/dendrites-compute-independently-of-cell-body/). Electromagnetic signals propagate through neurons, modulated by thousands of kinds of ions, chemicals, and other cells in the fluid around them. Neurons contribute to an overall electromagnetic field, as well as pressure and temperature fields that globally influence brain behavior.

Brains evolved as the electrochemical control systems that help control our bodily movements and functions. Along the way, they evolved perception, intelligence, and consciousness to aid control. Computers are the opposite: they were invented and engineered for logical calculation, but then could be applied to robotic control, among other things.

From this high-level view, it is hard to find much at all in common between computers and brains. Computers are built on modular digital logic, brains are "built" on inseparable continuous systems and nonlinear dynamics.  Computers have effective layer abstractions, so that you can understand one layer while ignoring the others, e.g., you can write software without knowing the hardware architecture. Brains have no such layer abstraction. Computers have discrete clock cycles, so that all logic operations happen in a rigid lock-step. Brains do not operate according to such discrete clocks. Computer software can be paused and restarted in a hundred years, and continue with no apparent pause. You cannot "pause" a human without killing them.

All Turing-equivalent computers are based on some sort of symbol manipulation, like binary voltages. The brain does not seem to be based on a discrete representation—even [neuronal spike trains convey continuous information](https://www.biorxiv.org/content/10.64898/2026.09.15.751814v1). 

Brains are part of living organisms, computers are not.

If computers and brains shared some meaningful mechanisms, then we might reasonably expect them to share other attributes. But **biological and computer substrates differ in every meaningful way**. So it would actually be quite surprising if consciousness naturally generalized from brains to computers, just based on substrate.

I suspect that consciousness comes from some overall physical system properties, some dynamical overall electrochemical state of brain regions and chemicals (e.g., oxytocin, cortisol). (This might be the subject of a future blog post.) Consciousness is not the setting of variables in general-purpose memory storage; it is about the physics and the biology. To paraphrase neuroscientist Anil Seth, who advocates for this view of consciousness: you cannot separate what a brain is from what it does, and this lack of separability seems important for consciousness. Even though we do not know how the physics produces consciousness, but this idea of consciousness as electrochemical system state fits the evidence well.

Sometimes when people say "the brain is a computer," they seem to mean that the brain might not be Turing-equivalent, but it is still a machine for processing sensory data and controlling actions. This might be accurate, but, if so, it means that the brain is not Turing-computable, and so something that cannot be replicated in our digital computers (e.g., ["super-Turing" functions](https://www.science.org/doi/abs/10.1126/science.268.5210.545)). Hence, this is not an argument for conscious AI on digital computers.

These vast differences between brains and computers encourage extreme skepticism about computer consciousness. But it does not rule out the possibility that consciousness comes solely from some sort of higher-level processing. I'll discuss this is the next few sections.



<center>
	<figure>
			<img src="../../../images/brains/microprocessor.jpg" height="224" width="480">
		<figcaption><i>Some of the different abstraction levels in a microprocessor: 
Instruction fetching and execution; typical circuits like adders; logic gates; transistors; silicon chip that conducts electric current.
(<a href="https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005268">Source</a>)
			</i>
		</figcaption>
	</figure>
</center>


# Brain processes as computations

We can describe many brain processes computationally; does this mean we can replace them with computation? 

For example, early vision cells (V1) compute image processing filters, and dopamine reward processes can be modeled by reinforcement learning theory. Many cognitive processes can be approximately described with the language of computing, such as [the blackboard system](https://en.wikipedia.org/wiki/Blackboard_system) that inspired [global workspace theory](https://en.wikipedia.org/wiki/Global_workspace_theory).  

These computational metaphors for neuroscience have been enormously powerful and successful at advancing the theory of neuroscience, cognitive science, and psychology. These successes themselves demonstrate the value of computational brain models.

But, just because we can describe a system as computation does not mean that it is _just_ computation. In fact, nearly every process in the world can be approximately described computationally, whether fluid flow, economics, spread of viruses, and so on. Does a flowing river "compute" computational fluid dynamics?  No, because water actually flows, and the system states cannot be read out of variables afterward.

Even if we had a perfect mathematical model for the brain regions that produce consciousness, computing that model would not necessarily produce consciousness.

<center>
	<figure>
		<img src="../../../images/brains/river.jpeg" width="480" height="S1364-66132500286-4">
		<figcaption><I>Flowing water does not compute the equations of fluid mechanics. The brain does not compute neuronal dynamics or the equations of reinforcement learning.</I>
	</figcaption>
</figure>
</center>

# Could computation produce consciousness?

This brings us to a general argument that consciousness cannot arise from digital computation, regardless of the form. 

[In a classic joke](https://www.math.mcgill.ca/rags/JAC/mathjokes.html), an engineer, a chemist, and a logician are staying in a hotel. In the middle of the night, a fire breaks out in the hallway. The engineer is woken up by the smoke, fills a bucket of water, throws it on the fire, and goes back to bed. Another fire wakes the chemist, who mixes up a fire-retardant formula, sprays it on the fire, and goes back to bed. A third fire wakes the logician, who notices a fire extinguisher on the wall, proves that the fire can be extinguished, says “good, a solution exists,” then goes back to bed.

The point here is that some things are outside the realm of pure logic. A fire extinguisher can put out a fire, but logical reasoning about it cannot. [Likewise, a computer simulation of fire cannot burn down your house](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/abs/mindsbrainsandprograms/DC644B47A4299C637C89772FACC2706A).

Yet, some things are within the realm of pure logic. [A simulation of a calculator is still a calculator](https://www.thinkinghard.com/blog/WhenIsASimulation). 

Which kind is consciousness? 

Conscious experiences and feelings are outside the realm of pure logic. Logic operates on symbols that can be assigned true values, and it derives truth values for other symbols. We can think logically about consciousness, but applying logical formulae like `A OR B` does not _produce_ consciousness, just like hand-computing the equations of heat transfer won't cause your pencil to burst into flames. 

And, as we've already seen, _all_ computation boils down to logical calculation.  If applying pure logical calculations cannot produce consciousness, then computation cannot produce consciousness.

Likewise, artificial neural networks are simple mathematical operations—often not much more than large matrix operations—approximated in digital logic by floating-point arithmetic. Again, it seems implausible to me (and to many people) that approximate matrix multiplications will generate consciousness, whether worked out by hand on the page or computed by computer logic.

This experience that you're having right now, whatever feelings and sense of self you have—how could it be that these experiences happen _because_ your brain is calculating logical equations or applying mathematical formulae?

Now, you might ask the same question about the electrochemical mechanisms in the human brain—how could these produce consciousness? And, yet, (a) we know that they somehow do because we experience consciousness, and (b) they employ entirely different mechanisms from computer logic circuits. So the fact that we do not know how consciousness arises in brain mechanisms is not itself a good argument that any other system can produce consciousness.





<center>
	<figure>
			<img src="../../../images/brains/calculator.jpg" height="360" width="339">
		<figcaption><i>Not conscious.		</i>
		</figcaption>
	</figure>
</center>



# Theories of computational consciousness and "cheap consciousness"

In all of history, no human-made object has ever been conscious. We would need very good reason to believe that this has changed. In the words of a famous rule: [extraordinary claims require extraordinary evidence.](https://en.wikipedia.org/wiki/Extraordinary_claims_require_extraordinary_evidence) Humans creating consciousness for the first time in history would surely be extraordinary. So what are the serious arguments for computational consciousness?

[Some people claim](https://www.ingentaconnect.com/content/imp/jcs/2016/00000023/f0020011/art00002) that the special feeling of consciousness, as an innate, private, set of experiences, is itself illusory. That is, it's just ordinary information processing that the brain reports as experience. But this just reraises the question: what does it take to create that "illusion of feeling"? Could you implement such a report in a computer and then believe that the computer is conscious?

This brings me to the idea of [_"cheap consciousness."_](https://philarchive.org/rec/MICOCA-3) If you give me _any_ sufficiently detailed theory of how consciousness arises from computation, then I can write a simple computer program that embodies that theory. Then you would have to accept that that computer program is conscious. For example, according to the illusory consciousness idea, if I write a short, 10-line program that "reports information processing as experience," then the program ought to be conscious. 

If you believe that consciousness requires [a global workspace, recurrent processing, and attention](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-6613(25)00286-4), then I can build a simple program that embodies all of those features. I bet that self-driving cars already do satisfy the most-popular criteria for AI consciousness. The exception would be if your theory requires large-scale systems and emergence, which I will discuss in the next section.

Some of these theories acknowledge the problem. For example, in [Butlin et al.'s proposal for detecting AI consciousness](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-66132500286-4), they explicitly state that indicators should be designed to prevent "gaming" by trivial instantiations of consciousness theories. But they do not explain how this is possible, i.e., how can you tell when consciousness theory goes from "cheap" to "real"? I suspect it cannot be done.

All of these ideas defer the question of how a sequence of logical operations could "produce experience." More broadly, prominent works like [Butlin et al.'s paper](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-66132500286-4) or [the claim of global workspaces in an artificial neural network](https://arxiv.org/abs/2607.15495) do not attempt to demonstrate for the existence of computational consciousness, they simply make it a working assumption.

Some authors [do explicitly argue that](https://arxiv.org/abs/2411.00986) that "that there is a realistic possibility that some AI systems will be conscious and/or robustly agentic in the near future." Their primary argument seems to be a list of computational theories of consciousness.

These arguments are quite speculative, and none provide the extraordinary evidence or reasoning required to make computer consciousness a realistic possibility, to convince us that for the first time in the history of humanity, we will make (or have made) conscious things.

After all, for a computer to create real things solely by logical reasoning would be sorcery.


<center>
	<figure>
		<div style="display: flex; justify-content: center; align-items: flex-end; gap: 8px;">
			<img src="../../../images/brains/apprentice-stars.jpg" height="240" width="338">
			<img src="../../../images/brains/apprentice-water.jpg" height="180" width="241">
		</div>
		<figcaption><i>Creating stars or consciousness merely from logical reasoning would be literal sorcery.</i>
		</figcaption>
	</figure>
</center>






# Practical problems if there is consciousness is computational

Now let us suppose that I'm wrong, and, in fact, computation alone can produce consciousness.  This alone does not demonstrate practical AI consciousness; we would also need to be able to implement it on modern computers in the foreseeable future. 

I still believe we can rule out consciousness of simple computer programs; how could a few logical computations be conscious? But suppose consciousness is an emergent property of large-scale computations. _Emergence_ describes complex properties of systems that are only apparent in large-scale systems, but cannot be identified just by looking at individual elements of the system. 

If so, how much computing power would emergent consciousness need? This is a head-scratcher, since we don't have a good way to quantify these things. But, surely, it would take a whole lot more than we've got running individual AI models now.

One approach is to consider simulation of the human brain as an upper bound on the computation required. But, as I discussed [in a previous blog post](/2026/07/13/brain-not-a-computer.html), fully simulating the brain is a wildly infeasible idea, since it is so enormously complex, involving 86 billion neurons, each of which is like a complex analog computer, with thousands of dendrites, [each having their own learning and memory dynamics](https://www.thetransmitter.org/memory/dendrites-compute-independently-of-cell-body/), as well as thousands of ion channels, influencing signalling through chemical and hormone interactions, glia, electromagnetic fields, fluid dynamics, and so much more.

One practical problem is that computation is wildly energy-inefficient compared to biological brains. [One analysis suggests](https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2023.1240653/full) the amount of power consumption required to approximately simulate the human brain in real-time is greater than all power consumption in the United States.

Of course, in this hypothetical, we don't need to fully simulate the brain to produce consciousness. But consciousness is a continual, ongoing, rich experience. (Various illusions indicate that our perceptions aren't as accurate as they seem, but the experience itself is quite rich regardless.) Moreover, we probably don't care too much about "small amounts of consciousness," like a computer that has the consciousness equivalent to, say, a fruit fly. Getting meaningful emergent consciousness anywhere in the realm of human consciousness would nonetheless seem to require massive datacenters worth of computation. 

But this reasoning is primarily science fiction hypotheticals, and so I think our defaults—that things are not conscious—should take over.

<center>
	<figure><a href="../../../images/brains/energy_use.jpeg"><img src="../../../images/brains/energy_use.jpeg" width="480" height="386"></a>
	</figure>
	<figcaption><I>Estimates of power consumption required for real-time brain simulation, from <a href="https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2023.1240653/full">Stieffel and Coggan</a>, using simplified brain models. In their estimate, human brain simulation would require more than the entire US power output.
	</I></figcaption>
</center>

# Could we build conscious machines some other way?

What if we abandon digital computing, and use solely analog electrical circuits, as in ideas like [neuromorphic computing](https://en.wikipedia.org/wiki/Neuromorphic_computing) and [mortal computing](https://arxiv.org/abs/2311.09589)? Could engineered systems that abandon digital abstractions produce consciousness?  Doing so would overcome most of my objections so far.

However, the answer to those questions does not matter to the topic of whether AI could be conscious in the foreseeable future, because no one has built a plausible AI system on analog computing. This is back to the realm of science fiction hypotheticals.



# Putting it together: the improbability of conscious AI

The progress of computing and AI has been truly amazing in the past decade: the ability of algorithms to process data and produce potentially useful outputs has been truly astounding. None of this, however, demonstrates that they should gain new capabilities entirely outside of the realm of computation and logic, and, I believe that consciousness is one of these capabilities.

To recap, the argument that modern computers cannot be conscious has the following parts:

1. **We can reason about consciousness in humans and animals,** based on behavior and mechanisms, along with our own experiences of consciousness. Behaviors alone are not sufficient to prove anything, since they can be faked.

2. **Only animals are known to be conscious; never in  history have we created conscious objects.** Hence, conscious human-made objects would be an extraordinary development, and so we should be very skeptical of it. It would require extraordinary reasoning and/or evidence to justify.

3. **Brains are the only conscious things we know, but the physical properties of brains and computers have essentially nothing in common.**  And, the differences are relevant: biological brains are inseparable from organisms evolved for survival, whereas computers are modular, layered human-made machines based on symbolic logic. Consciousness probably arises from basic physical states of the brain, not from a set of logical variables encoded in memory.

4. Even if it does not depend on brain physics and chemistry, **consciousness lies outside of the realm of logic and computation**: consciousness is not a logic construct, and all computation is reducible to logical calculations. Hence, performing logical calculations cannot produce consciousness, any more than fluid simulation produces water. 

5. Moreover, **if you give me a computational theory of consciousness, I can write a simple computer program that fits the theory,** leading to the untenable view that simple programs can be conscious. This contradicts typical theories of computational consciousness.

6. Even if computers could be conscious, it would probably be an emergent property, requiring **impractical amounts of computer power.**

Together I believe these arguments show that conscious AI with modern computing is profoundly unlikely in the foreseeable future. 

Computer consciousness is a fascinating thought experiment,  philosophical problem, and [science fiction premise](/2026/08/05/science-fiction-ai.html). But it is not a practical concern.

Perhaps it could happen in 50 years; who can say anything about 50 years of technological development? But it won't happen in 5.


# Against "conscious AI is possible"

A common posture these days is to say "conscious AI is possible", and that we do not know for sure either way. While true, such statements give the misleading impression of a balance of probability, that conscious AI is a _reasonable near-term possibility_. Maybe even the products you can buy now are conscious. 

The term "AI" has collapsed in modern discussion to mean just a few things, despite its 60+-year history of meaning many different things. A philosopher might discuss hypothetical future AI involving unforeseen technological breakthroughs, and a modern listener might think that their comments mean it could happen any day now.

Such balance-of-probability statements are dangerous when they influence behaviors, such as when they let people believe they're talking to a conscious agent that cares about them, or when people argue for the moral value of AI research and development, or focus energy on the wellbeing of AI agents, rather than the humans affected by AI technologies.

I have argued that the possibility is so infinitesimal as to not be worth thinking about. We might as well worry about aliens landing on Earth next year and demanding enormous tributes of cheese. I mean, this is really unlikely, but can you prove it won't happen?

Likewise, we should not say that "conscious AI is possible" without also adding "... but it is profoundly unlikely in the foreseeable future."



# References and philosophy jargon

An excellent starting point for current thinking on these topics is [a recent paper by Anil Seth and its fifty commentaries](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/stuff-matters-consciousness-computation-and-biology/E6C81A819898C25A43C7BD1F0752B1FF#related-commentarie).  It's tough reading, with concepts scattered about in lots of ways, but nonetheless an amazing collection of useful readings, and many ideas here are drawn from that paper, commentary, and/or the papers they cite.

My previous blog post on [why brains are not just computers](/2026/07/13/brain-not-a-computer.html) drew directly on [Rosa Cao's work](https://link.springer.com/article/10.1007/s11229-022-03524-1), as does this one.

The main topic here is "functionalism," the idea that consciousness emerges from how the brain works. "Computational functionalism" is the view that consciousness requires the right kinds of computations, so any computing device could be conscious. 

While I haven't gone into depth about alternatives here, I  have briefly argued here for a form of "non-computational functionalism," in which consciousness requires specific physical properties, and computation alone can't provide them. (This could be a future blog post.) I believe in "substrate dependence:" it seems improbable that any sort of non-biological substrate could attain the kind of physical properties necessary for consciousness. I lean toward "Biological naturalism," the idea that only biological organisms can be conscious. (I'm intrigued by  ideas that treat [life itself as a distinct state of matter](https://thereader.mitpress.mit.edu/is-life-itself-a-state-of-matter/), and/or [a product of the second law of thermodynamics](https://press.uchicago.edu/ucp/books/book/chicago/I/bo3533936.html).)

["Triviality"](https://marksprevak.com/publications/triviality-arguments-about-computational-implementation-2018/) is the observation that a physical system has an infinite number of distinct interpretations as computation. [Papayannopoulos gives a compelling example with simple logic circuits](https://link.springer.com/article/10.1007/s10539-022-09877-8). Hence, there is no objective way to interpret a physical system as performing a specific computation.

[John Searle originated the analogy](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/abs/mindsbrainsandprograms/DC644B47A4299C637C89772FACC2706A) that a simulated fire does not burn down your neighborhood, nor does a simulated thunderstorm doesn't make your computer wet. It's a useful analogy, but I think that the way he presented it misses the mark a bit, since no one thinks that AI is "simulation." Still, it offered a useful starting point for some of these thoughts, as did [Tim van Gelder's steam governor analogy](https://www.jstor.org/stable/2941061).

The idea of the brain as a controller goes back, at least in some form, to [Jakob von Uexküll](https://en.wikipedia.org/wiki/Jakob_Johann_von_Uexk%C3%BCll).

The idea that consciousness isn't an innate private experience, but is how the brain reports experiences to itself is ["illusionism"](https://www.ingentaconnect.com/content/imp/jcs/2016/00000023/f0020011/art00002). Illusionism does not require computational functionalism; it is compatible with biological naturalisms.

[Peter Godfrey-Smith has written about the biological evolution of intelligence and consciousness from control](https://www.jstor.org/stable/48568275), and how different organisms experience different forms of consciousness; see especially his book _Other Minds_.


# A final note

This essay was written in the company of my dog Cinco, who demonstrates that [you don't have to be an "intelligent agent" to be conscious and loving](/2026/05/15/dog-knowledge.html).