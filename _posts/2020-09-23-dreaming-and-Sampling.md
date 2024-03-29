---
layout: page
summary: How dreams could be gradient updates
author:  AaronHertzmann
image: /images/goya.jpg
---

# Dreaming and Sampling

I just read Borges' "Nightmares," a lecture from 1977 in which he grappled with the nature of dreaming. Whenever I think about the nature of dreams, I always think of a theory that Geoff Hinton told me long ago, probably 15 years ago. Geoff told it in his typical tone of conviction laced with ironic self-awareness about that conviction.

One thing our brains need to learn is how likely are things to appear in the world, and what are likelihood outcomes of sequences of events. That is, we need to learn a probability distribution over possible experiences we could have.  In Maximum Likelihood learning, we seek to set model parameters to learn the probability that our brain assigns to different outcomes.

Through some clever math, one can rearrange the negative log-likelihood to have two terms<sup>1</sup>: the "energy" of the evidence that you did see, and the expected "energy" of every possible occurrence that you didn't see. Learning is about trading off these two terms, which automatically trade-off between predicting the things you saw and not the things you didn't see.

In Geoff's theory, during waking, we gather our daily experiences as positive examples and use them to take gradient steps to update the first term.  During sleep, we randomly sample sequences of events from our current model of the world, so that we can take gradient steps to downweight these scenarios. In other words, **in a dream our brain explores scenarios that it believes to be likely, and then updates its beliefs so that these scenarios are _less likely_,** because, after all, we didn't actually experience them during the day. 

He said that his theory predicted that updating neural weights during dreaming should proceed in reverse order in the brain. He said neuroscientists later discovered this reversed-time updated, and they were confused by it.

I have no idea if Geoff's theory has the slightest kernel of truth in it. I also don't know if he still believes it, or if he ever published it<sup>2</sup>.

Borges said, when introducing [J. W. Dunne's theories of dreaming](https://en.wikipedia.org/wiki/An_Experiment_with_Time), "I do not agree with this theory, but it is so beautiful it is worth recalling."  There is a lot about dreaming that doesn't seem to me to be explained by Geoff's theory.  But Geoff's theory is so beautiful it is worth recalling.

<center>
<figure>
  <img src="../../../images/arthistory/goya.jpg" alt="Goya etching"/>
  <figcaption align="center"><i>Random samples appear</i></figcaption>
</figure>
</center>


<BR>
<BR>
<BR>

---

<sup>1</sup>I think this might be the [Wake-Sleep Algorithm](https://en.wikipedia.org/wiki/Wake-sleep_algorithm). It somehow seems related to [predictive coding](https://en.wikipedia.org/wiki/Predictive_coding).

<sup>2</sup>The great thing about blogging is that you don't have to do a literature search, you can just say "I don't know."