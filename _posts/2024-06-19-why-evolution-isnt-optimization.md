# Why Evolution Isn't Just Optimization


As a computer scientist, it's natural to think of evolution as a [numerical optimization](https://en.wikipedia.org/wiki/Mathematical_optimization) process. After all, the process of Darwinian natural selection looks a lot like optimization: if two related genotypes give different outcomes—one is slightly more successful than the other in survival, than Darwin favors the former one.  There are so many aspects of our lives that seem to be perfectly fine-tuned.  So, for many of us, it is tempting to say that "evolution _is_ optimization." The biologists say this is wrong, but it's taken me awhile to come to understand why, while still acknowledging the power of optimization in modelind biological systems and real life. 

This post is attempt to explain some reasons that evolution is not optimization, even though optimization is often a useful tool.  Note that **I am not a biologist and not an expert in these topics** and so this might not accurately represent that viewpoint. My goal here is to point out some important distinctions between evolution and optimization.


# Why it's a useful model

I do believe that optimization is a **useful** model for many biological processes that are produced by evolution, as has been argued by many biologists, e.g., ([1](https://www.nature.com/articles/348027a0), [2](https://press.princeton.edu/books/paperback/9780691027982/optima-for-animals), [3](https://www.nature.com/articles/35088155), [4](https://www.nature.com/articles/435569a), [5](https://www.annualreviews.org/content/journals/10.1146/annurev.bb.16.060187.002323)).  


Although evolution solely optimizes the reproductive fitness of an organism, in practice we often model more easily-measurable quantities as being optimized. So many different aspects of biological systems, from bone density to jumping distances to the photoreceptive sensitivies of cones in the retina, to cognitive inferences, all seem to perfectly optimize the relevant constraints in a system, whether minimizing energy consumption or [Bayesian surprise](https://www.nature.com/articles/nrn2787). 

It's natural to think of individual behaviors as optimizing. Consider learning a new skill, like learning to catch a ball or cook an omelette. When you first do try it, you may be slow and awkward; after many, many repetitions, your movements become streamlined and efficient.  Basic skills like learning to walk become fluid and automatic.

For example, in one paper in 2005, [we modeled human motion synthesis as a biomechanical optimization problem](https://grail.cs.washington.edu/projects/charanim/phys-style.html). Like previous works in animation and biomechanics, we generated motions by minimizing some approximation of energy consumption.  Moreover, we could learn the optimization parameters from data, and then predict how an individual might walk under new constraints. This showed one way to make optimization predictive, not just fitting the data, but showing how someone might move under new circumstances.  In subsequent papers, we showed how to [optimize controllers for locomotion](https://www.dgp.toronto.edu/~jmwang/optuie/), and [how to generalize the loss functions to account for uncertainties](https://www.dgp.toronto.edu/~jmwang/optwalk/). There's been tons of work before and since then that optimizes motions as well.

(In the [Free Energy Principle](https://www.nature.com/articles/nrn2787), Karl Friston does seem to directly tie optimal behavior to evolutionary fitness, so maybe he would make stronger claims about evolution as producing optimality. There's also [the head-spinning idea that evolution is a consequence of the 2nd Law of Thermodynamics](http://www.ler.esalq.usp.br/aulas/lce1302/life_as_a_manifestation.pdf), which are fascinating but hard to relate to this discussion.)


# Why it's not a complete model


What it would mean to say that "evolution _is_ optimization"? The argument might be something like this: natural selection continually selects for fitter members of a population, just like an optimization algorithm. Evolutionary pressure over millenia naturally guides every population to select the fittest members, which, in turn, perfects every aspect of an organism, e.g., with optimal gaits, optimal bone densities, and so on. 

If this were the case, then we might expect to see much less diversity of creatures and species than we see today.  Here I think it's easiest to simply quote wholesale from [this FAQ on evolution from Berkeley](https://evolution.berkeley.edu/teach-evolution/misconceptions-about-evolution):
<ul>
	Natural selection does not produce organisms perfectly suited to their environments. It often allows the survival of individuals with a range of traits — individuals that are “good enough” to survive. Hence, evolutionary change is not always necessary for species to persist. Many taxa (like some mosses, fungi, sharks, opossums, and crayfish) have changed little physically over great expanses of time.
</ul>

More fundamentally, the optimization account requires a fixed objective function. But the world is always changing, though often on very slow time-scales, with changes to environments and climates. An organism that is "optimal" one year may no longer be optimal the next.  An individual perfectly optimized for one fixed environment may be fragile to environmental changes.  The Berkeley FAQ again:
<ul>
	The whole idea of “progress” doesn’t make sense when it comes to evolution. Climates change, rivers shift course, new competitors invade — and an organism with traits that are beneficial in one situation may be poorly equipped for survival when the environment changes.
</ul>

One could  counter: organisms are optimized for _robustness_, that is, they don't just optimize fitness for a current moment, but also to respond to enviromental changes. We keep around suboptimal mutations and variants because they might save our bacon in the future.  It's unclear that this "optimization" could be modeled mathematically; it's certainly not the optimization that we normally think about.  There's no individual moment in which we measure optimality, but a continual process of change and evolution. Perhaps the notion of "optimization" could be expanded this way (as in [continual learning](https://arxiv.org/abs/2302.00487)), but then it's barely optimization if there's no single loss.

There are also some biological changes that just don't seem to be adaptive, resulting instead from random changes.
<ul>Mutation, migration, and genetic drift may cause populations to evolve in ways that are actually harmful overall or make them less suitable for their environments. For example, the Afrikaner population of South Africa has an unusually high frequency of the gene responsible for Huntington’s disease because the gene version drifted to high frequency as the population grew from a small starting population.
</ul>

If evolution were really optimization, then we might expect that only one organism lived on Earth: the Optimal Creature. But that's not how evolution has operated; it has produced an amazing diversity of organisms, each filling their own niches.  Our organisms co-exist in complex, interdependent ecologies. We could not survive on this planet alone, dependent on everything from the plants and animals to the gut bacteria that we co-evolved with.

An optimization theory, moreover, suggests that fitness is being explicitly measured somehow, that it is a real thing.  But there is no prime mover or guiding hand. Evolution has _just happened_ as a product of physical laws, of random events in the world.  There is no explicit optimization mechanism.  

Perhaps much of this process can be _modeled_ by optimization, but as a comprehensive theory it doesn't seem possible to do so in a meaningful useful way.




# AI and Why It Matters

Us computer scientists often don't care about these distinctions because we're just trying to model individual behaviors; we don't usually care much about actual modeling of the diversity of life. Biologists, on the other hand, are trying to explain real systems, fully, and there are many crucial elements of biological evolution that don't fit into a simple optimization paradigm.

Some biologists may be particularly sensitive because "optimization" implies that someone out there has specified an objective function, which reeks of creationism. Being scientifically precise isn't just a matter of niceties, it's an unfortunate necessity in some of the culture wars.

The evolution-optimization distinction matters when we start trying to make claims about "artificial intelligence."  Human intelligence and AI are both the product of optimization, and so they're basically the same, claims one staggeringly-false equivalence.  This is just one example of the typical [lazy false equivalences](/2022/09/04/computationalism.html) made between human and artificial intelligence, often born of [misleading terminology](https://arxiv.org/abs/2104.12871). We can model aspects of human learning as optimization, but this does not mean that it is equivalent to any other optimization-based learning.

