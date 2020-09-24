# Dreaming and Sampling

I just read Borges' "Nightmares" for the first time, where he grapples with the nature of dreaming. Whenever I think about the nature of dreams, I always think of a theory that Geoff Hinton told me long ago, probably 15 years ago. Geoff told it in his typical tone of conviction laced with ironic self-awareness about that conviction.

One thing our brains need to learn is how likely are things to appear in the world, and what are likelihood outcomes of sequences of events. That is, we need to learn a probability distribution over the world.  In Maximum Likelihood learning, we seek to set model parameters to learn the probability that our brain assigns to different outcomes:

Through some clever math, one can rearrange the negative log-likelihood to have two terms<sup>1<sup> : the probability of the evidence that you did see, and the expected likelihood of every possible occurrence that you didn't see. This expectation cannot be computed.

In Geoff's theory, during waking, we gather our daily experiences as positive examples and use them to take gradient steps to update the first term.  During sleep, we randomly sample sequences of events from our current model of the world, so that we can take gradient steps to downweight these scenarios. In other words, in a dream our brain is exploring what it believes to be likely, and then updating its beliefs so that this scenario is _less likely_, because, after all, we didn't see them during the day. 

He said that his theory predicted that learning from dreams should proceed in reverse order in the brain, something that had later been discovered by neuroscientists to be true.

I have no idea if Geoff's theory has the slightest kernel of truth in it.

Borges writes, about [J. W. Dunne's theories](https://en.wikipedia.org/wiki/An_Experiment_with_Time), "I do not agree with this theory, but it is so beautiful it is worth recalling."  There is a lot about dreaming that doesn't seem to me to be explained by Geoff's theory.  But Geoff's theory is beautiful, so I am content to remain ignorant about the science of dreaming and to believe in it.

---

<sup>1</sup>If I recall correctly, this was the foundation of [his Boltzmann Machine learning algorithm](https://en.wikipedia.org/wiki/Boltzmann_machine#Training), and later [Contrastive Divergence](https://www.cs.toronto.edu/~hinton/absps/tr00-004.pdf) (which insired our own [Inverse Optimization](http://grail.cs.washington.edu/projects/charanim/phys-style.html) algorithm). It somehow seems related to [predictive coding](https://en.wikipedia.org/wiki/Predictive_coding), which I haven't studied carefully.
