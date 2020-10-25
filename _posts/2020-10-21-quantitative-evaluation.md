---
layout: page
summary: Sometimes computer vision reviewers focus too much on scores, especially for image synthesis papers.
author:  AaronHertzmann
---


# Quantitative Evaluation Isn't Everything

*"Who are you going to believe, the numerical scores or your own eyes?" — [The Marx Brothers, sort of](https://www.youtube.com/watch?v=cHxGUe1cjzM).*


Computer vision paper reviewers generally expect that paper submissions will have quantitative evaluations, typically, a table of numbers showing that the proposed method outperforms the state-of-the-art on some dataset. **I think that computer vision reviewers are overly obsessed with quantitative evaluation in a way that can hurt the field.** 

Why We Perform Quantitative Evaluation
---

As a bit of background, quantitative evaluation has been crucial to progress in the field. Around two decades or so ago, most vision papers typically showed results on their own data, or on the same few images, or on some synthetic benchmarks. At some point, there were enough competing methods that it became difficult to tell which methods were making advances. So a number of authors created benchmarks, notably the [Middlebury datasets](https://vision.middlebury.edu/stereo/data/) and [Caltech-101](http://www.vision.caltech.edu/Image_Datasets/Caltech101/), among others. 
It was still a common joke among many researchers that "computer vision doesn't really work," and the idea that any of this would be useful anytime soon seemed like pure fantasy.
As recognition algorithms got better, the need for more substantial benchmarks led to the monumental [ImageNet benchmark](https://en.wikipedia.org/wiki/ImageNet). This dataset in turn led to the rise of deep learning in computer vision, and things got real crazy real fast. For better or for worse, benchmark evaluation was essential to the success of the field. (There are also numerous legitimate criticisms of harms and biases of these datasets which are not my topic here.)

In subfields of vision with many existing methods with clear metrics, quantitative evaluation is crucial. For example, if you want to propose a new depth estimation method, then you ought to compare your method to the latest methods, and you should use standard benchmarks and evaluation metrics to do so. It's not hard to do, and, without this evaluation, it's too hard to tell if the new method is contributing anything.

However, focusing solely on these numbers can distort research. It is always important to remember that **quantitative evaluation never measures what we actually care about.**  Every metric is a proxy for things like real-world performance, and every dataset has bias.  Metrics based on average performance may downplay the costs of very bad failure cases. Moveover, **focusing too much on evaluation makes creative, exploratory work difficult,** because very novel ideas are unlikely to fare competitively against established, highly-polished methods. Finally, the expectations for evaluation when proposing worthwhile new tasks or problems needn't be very high, as compared to work that proposes refinements on existing problems.


This is not a unique problem
---

None of these are new observations. Here are some papers I recommend that discuss this or related topics in various contexts:

**[The CVPR 2011 paper by Torralba and Efros on biases in benchmark datasets and evaluations](http://people.csail.mit.edu/torralba/publications/datasets_cvpr11.pdf) is well worth revisiting today**.

**[My NPAR 2010 paper (Section 3)](http://www.dgp.toronto.edu/~hertzman/ScienceOfArt/) discusses the dangers of reliance on quantitative evaluation** in the context of artistic image synthesis and stylization.

**In the past decade, a [Replication Crisis](https://en.wikipedia.org/wiki/Replication_crisis) has shaken many fields of science, most prominently psychology.** One of the causes is the reliance on a single numerical score for judging paper acceptances: the *p*-values of null-hypothesis significance testing (NHST).  [This early paper from the crisis discussed](https://journals.sagepub.com/doi/10.1177/0956797611417632) some ways that researchers can unintentionally overfit to a single metric.  One large-scale study conducted an ambitious program to attempt to reproduce results from 100 psychology papers, and [was able to find significant results for 36% of them](https://science.sciencemag.org/content/349/6251/aac4716). In response to this controversy, many psychology journals have restricted the use of NHST, or they make acceptance decisions *before* seeing the experimental results. 

**[This recent essay warns of a replication crisis in computer science,](https://cacm.acm.org/magazines/2020/8/246369-threats-of-a-replication-crisis-in-empirical-computer-science/fulltext)** primarily focused around NHST and *p*-values, but the discussion may also be relevant to other forms of quantitative evaluation.

**[Greenberg and Buxton explain how an over-reliance on user testing in HCI research](https://www.billbuxton.com/usabilityHarmful.pdf) can discourage and prevent publication of more creative, exploratory research.**

A general rule of thumb I've heard from computer vision researchers is that a dataset loses its usefulness one people are getting very good scores on it, say, 95% accuracy. At that point, the dataset is "saturated" and further improvement on it doesn't mean anything.

More broadly, the way that measurement-based incentive structures can fail society is a broader topic, e.g., this is a major theme of the TV show The Wire; see also [Goodheart's Law](https://www.nature.com/news/watch-out-for-cheats-in-citation-game-1.20246).


Image Synthesis and Graphics Papers
---

When I began research in computer graphics, very few papers included any quantitative evaluation at all. It was enough to show images and results. Generally speaking, you explain the visual phenomena being modeled, and then let the viewer see for themselves how well you've captured it. Very few of the most significant or influential papers in graphics had any quantitative evaluation.  (Papers focused on algorithmic efficiency are an exception.)  Looking back at my own papers, the first SIGGRAPH paper I published with any numbers at all came 3 years after I finished my PhD, and those numbers weren't determined in a rigorous manner at all.

Unfortunately, the expectations of user evaluation grew at SIGGRAPH. So-called "user studies" started appearing to evaluate the results (they would be more accurately called "user evaluations" or "perceptual studies," depending). These studies can be useful as a way to provide evidence that the results you're showing in the figures generalize to larger datasets. But often they are a crutch to avoid looking at the pictures critically. 

Worse, sometimes asking for "user studies" is a crutch for reviewers to avoid making a hard decision. Instead of saying "we don't believe this method is worth publishing here" they say "maybe a user study would convince us" when it almost certainly would not: this feedback is harmful, since it can falsely raise authors' hopes.

And, many "user studies" in the graphics and vision literature are so poorly conducted that they are barely useful at all.  Certainly, computer vision authors are not trained in running rigorous psychology studies, and there are many ways to bias studies results if you're not careful. 

(For broader discussion of image synthesis in computer vision, you may be interested in [my CVPR 2020 workshop talk](https://www.youtube.com/watch?v=wCRJBy_LPVY).)

Two recent examples
---
Here are two examples from my own recent computer vision publications. Each paper was rejected from a vision conference (at least partly) on the basis of quantitative evaluation before being accepted on a resubmission.


[**Our GANSpace paper**](https://arxiv.org/abs/2004.02546) includes new user interfaces for exploring and controlling GANs.  We included extensive sets of images [and video](https://www.youtube.com/watch?v=jdTICDa_eAI) that visualize what our method finds; we believed that this was sufficient to demonstrate that the paper is interesting enough to publish.  This paper was rejected from ECCV 2020 in large part because the lack of quantitative evaluation. The reviewers did not say what evaluation they thought would be useful, or what method we should compare to (there was no relevant baseline at the time), or why evaluation was necessary, or what question needed answering; they seemed simply to believe that all papers must have quantitative evaluation.  Fortunately, the NeurIPS 2020 reviewers were more receptive.

The issues in [our **paper on physics-based human motion estimation**](https://geometry.stanford.edu/projects/human-dynamics-eccv-2020/) are a little more subtle. In this case, there exist standard benchmarks and evaluations for the problem, and we reported scores on these benchmarks that were no better than those of previous methods.  However, our motions are much more physically plausible and they *look* much better than previous methods. This is because **the benchmarks measure the wrong thing** for several reasons. The benchmark was useful when errors were high, but not useful when errors are small.  One source of problems is that the **data used as "ground truth" itself suffers significant measurement error, and non-physical effects of the type our method was designed to fix**.  We showed results with different quantitative measures, based on previous methods in the biomechanics literature. However, the CVPR 2020 reviewers did not appreciate this argument; some focused entirely on the fact that our benchmark scores were no better than existing methods.  Fortunately, the ECCV 2020 reviewers were more receptive (it helped that we added scores from one more benchmark to the paper).

In each case, **it feels as if reviewers expect to see a table of numbers, and they expect to see that the numbers from the proposed method are better than the other papers' methods, without any critical thought as to whether the numbers are actually meaningful or useful.** Sometimes in project meetings I find myself saying "we gotta have some numbers in this paper," which I hate.


How to Judge Papers
---

**There is no such thing as objective evaluation of a technical paper. [Each paper must make a case as to why the ideas presented are valuable](/2020/07/13/rebuttals.html)**. Reviewers and ACs discuss and come to a consensus as to the potential benefit of publishing the paper.  Quantitative evaluation is usually an important part of the case, especially when there are meaningful benchmarks and metrics to evaluate on. But sometimes a convincing case can be made for the value of the paper just based on  arguments, theory, and/or images alone.  The authors must write convincingly to make this case. 

A good rule of thumb comes from Pierre-Simon Laplace, in his essay on Bayesian probability, paraphrased as ["Extraordinary claims require extraordinary evidence."](https://en.wikipedia.org/wiki/Sagan_standard) A complex and confusing method needs to show fantastic improvement in results, whereas an elegant and clear insight doesn't require as much evidence to demonstrate that it's worth publishing.  Sometimes a paper with superior scores should be rejected, for various possible reasons.

Another rule of thumb I've heard, from Maneesh Agrawala, is: an evaluation should be designed to answer a question. If you know the answer in advance, there's no point in performing the evaluation.  Quantitative evaluation is normally worthwhile because we can't really be sure if an idea that sounds good actually improves over previous methods.

The reviewers, for their part, must use their brains, and not just check to see if there's a table of numbers.
