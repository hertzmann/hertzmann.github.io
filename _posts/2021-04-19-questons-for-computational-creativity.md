---
layout: page
title: Questions for Computational Creativity Research
summary: I keep feeling like I'm missing something
author:  AaronHertzmann
image: /images/sims.jpg
---


# Questions for Computational Creativity Research


There's a small but active research community that works on computational creativity (CC). I haven't paid close attention to it, but it seems to comprise a group of eager and earnest researchers who are excited about this field, which is great.

Yet, I often find myself confused about the goals for the field.  For example, I was invited to speak at one of the workshops; I told the organizers that I was skeptical about this field, but they said they welcomed a critical perspective. In [my talk](https://youtu.be/qX9lLDOLG88?t=409), I asked some of these questions. While it was a very nice workshop, I left the workshop not feeling any closer to having any answers. (It's too bad the workshop had to be virtual, which makes these discussions much more difficult.)

Surely the people working in this field have thought about these questions and have answers–at least in their grant proposals–and I just haven't seen them. In any field, we motivate by some combination of vision, hopefulness, and proofs-of-concept, and maybe I'm just too blinkered to see those things here.  


Why study computational creativity?
=====

I can imagine several possible goals for CC research:

1. **Make  _algorithms that are considered creative_**
2. **Build tools to _support human creativity_** 
3. **Develop useful new algorithms _inspired by human creative behaviors_.**

Most of the CC papers I've looked at appear to be aiming for the first goal: making computers that are considered creative in some way. The second and third goals seem very worthwhile to me. **This blog post is mainly about the first goal.**

[This 2014 blog post by Anna Jordanous](https://www.creativitypost.com/article/what_is_computational_creativity) covers a lot of this territory about the goals for the field, and the various versions of the problem statement that different researchers and communities have asserted, as well as challenges in defining the problem.


Why could computers be themselves creative?
=====

What inspiration/belief drives this field? As this is research, we can't expect to have proof that CC is possible, but there ought to be some reason to believe, some persuasive story to tell about it.  

The main positive argument that I've seen is as follows. First, we should identify the attributes of a creative work, e.g., work must be both *valuable* and *surprising* or *original*. Then, if we can build a computer algorithm that does both of these things, then people will say that this system is creative. A much longer list of possible creative attributes appears in [a paper that received a ten-year award at ICCC](https://computationalcreativity.net/iccc2010/papers/jordanous-2.pdf).  

I would guess that there is a second inspiration that motivates some researchers: the delight and surprise that many of us have felt when seeing an unexpected output of a system. It feels magical when your algorithm produces results you didn't expect, sometimes [as the result of a bug](https://siggraphfails.tumblr.com/) that produces something wonderful, sometimes as the
result of [unintended consequences of your loss function](https://arxiv.org/abs/1803.03453), and sometimes simply as the result of a model that has a lot of parameters.  But then you go and figure out what the reason was, and it no longer seems so mysterious.


<center>
<figure>
<iframe width="560" height="315" src="https://www.youtube.com/embed/pxgLHuWfMS8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>  </iframe>
	<figcaption align="center"><i>
	Bloopers from Karl Sims' <a href="https://www.karlsims.com/evolved-virtual-creatures.html">Evolved Virtual Creatures</a>. "When first attempting to evolve locomotion behaviors, creatures were tested for their horizontal velocity during 10 seconds of simulation. They performed as requested, but in a much simpler way than what was hoped for. They simply became tall and rigid and fell over for most of the test duration."
</i>
 </figcaption>
</figure>
</center>

Are there other reasons to believe that the goal of creative computers is achievable? 


Haven't we already got results that are novel, surprising, and creative?
====

If the goal of this research is to produce outputs that are novel, useful, and/or surprising, don't we already have this? 

We already have algorithms that produce wonderful results in all sorts of domains, in images, music, animation, and so on. Whether or not this is the result of computer creativity is the issue.  

One statement of the goal of CC research is that [an observer would judge the results as "creative" had they been made by a human](https://www.sciencedirect.com/science/article/pii/S0950705106000645?via%3Dihub).  Yet, one method that achieved this goal years ago is [**Creative Sparks**](https://science.sciencemag.org/content/285/5433/1495.full), in which the authors described a very simple, easy-to-understand procedure for creating advertising concepts–the system could easily have been implmented by hand rather than with a computer. In a blinded study, marketers rated the resulting concepts as "more creative" than some pitches made entirely by individuals;
similar results are reported in [this paper](https://songweige.github.io/projects/creative_sketech_generation/home.html). 


Another statement of the goal of CC research is that [the creator of the system finds the results surprising](https://link.springer.com/chapter/10.1007/978-3-642-31727-9_1). I think we have this too. For example, the Mandelbrot set [can be summarized in just a few lines of code](https://en.wikipedia.org/wiki/Mandelbrot_set#Computer_drawings), yet it produces a seemingly-endless stream of mesmerizing imagery:
<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/PD2XgQOyCCk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>
that surely no one (including Mandelbrot) could have predicted from the math itself. Even after developing a rich theory of chaos and fractals, we can't really explain how "creative" it seems. By any formal definition of CC that I've seen, the Mandelbrot set algorithm is creative.


Indeed, many systems with simple rules can often demonstrate complex, emergent, seemingly-intelligent  behavior  (e.g., [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life), Mandelbrot set, [flocking](https://en.wikipedia.org/wiki/Flocking_(behavior))).

All the way back to Vera Molnár, who began work in the 1960s, describes [surprise as a major component of her generative art](https://opheliaming.medium.com/vera-moln%C3%A1r-the-computer-art-goddess-26a84efbea4b).  If you've written code to make images, you've probably been surprised at some point, and probably delightfully so at times.

Harold Cohen [went through similar stages](https://www.youtube.com/watch?v=_Xbt8lzWxIQ), first thinking that a procedural algorithm that made good artworks could be an artist, then realizing that all the works started to look similar, and then adding the additional criterion that the system must have its own changing worldview to be an artist. To me, this all looks like continually moving the goalposts.

**I think that process and context are crucial to judging creativity.** A painting is less impressive if you learn that it was done by filling in a [paint-by-numbers](https://en.wikipedia.org/wiki/Paint_by_number). If a person stumbles on a solution or an artistic style out of the blue, that's a whole lot more impressive than it if came after years of study of related solutions. (The [same point was made by Colton](https://www.aaai.org/Library/Symposia/Spring/2008/ss08-03-003.php).) Studies that show two images and ask blinded observers which is more creative or artistic have little value (possibly a topic for another blog post).
But, conversely, performing studies on AI-generated work [has its own problems](https://doi.org/10.1016/j.isci.2020.101515).




How could an automaton be creative?
====

Imagine the following thought experiment.

You hire an employee to create a Spanish-language poem, by following very specific rules. Your employee-who doesn't understand Spanish-must follow the rules precisely, to the letter, without deviation. The rules might be very complicated and involve rolling dice. In the end, the worker produces a poem that is widely lauded as original and wonderful. Is the worker creative? 

This is exactly the situation with computer algorithms: computers precisely follow our instructions, unfailingly without deviation. Unexpected results are due to the fundamental difficulty of predicting the outcomes of complex systems (and also due to bugs, and confusing APIs, etc).

Is it possible to be considered creative if you don't have [free will](https://en.wikipedia.org/wiki/Free_will)? I don't see how.

(This thought experiment above is similar to the ["Chinese room" argument](https://en.wikipedia.org/wiki/Chinese_room).)


Why is "creativity" a meaningful attribute?
====

The term "creative" seems very subjective.  Of course, we can do lots of research on subjective topics, but one has to be careful with terminology. We wouldn't attempt to formalize algorithms that make "beautiful" images; we might make algorithms that produce images that many viewers rate as aesthetically pleasing. Arguably, "creative" isn't a property of an image that can be separated from the process by which it was created. A printout of a famous painting is not itself creative, even if it is just as lovely as the original.

Personally, I think that "creative" is primarily a compliment that we give to people who made unexpected leaps of intuition. It's in the word itself: they "created" something, seemingly out of nothing.  We can say a lot of useful things about the behaviors of human creativity.  But this phenomenology is not the essence of creativity. If we could fully state the rules of creativity, we would not call it creativity any more, and maybe we will have disproven Free Will as well. Such an unlikely discovery would have massive enormous philosophical and practical implications beyond just making nice artworks.

Saying someone is "creative" is like saying that they're "talented." The word has some meaning. We could analyze the conditions under which people are described as "talented," and what are the behaviors of "talented people," but trying to develop "talented computing" would be equally quixotic.

Or one could read the book [The 7 Habits of Highly Effective People](https://en.wikipedia.org/wiki/The_7_Habits_of_Highly_Effective_People), and then use them to develop "effective algorithms." There are lots of other nonsensical applications of this kind of "definitional" approach to computational creativity and computational artists.



Why isn't this computer graphics/NLP/HCI?
=====

The technical content of most/all CC papers I've read (as opposed to theory papers) looks to me like it could have fit into the traditional research areas. Little about this work seems specific to CC research. For example, some papers present algorithms for synthesizing artistic images, which is common in computer graphics research.  [HCI research has an extensive history of directly studying human creativity and how computers can support it](https://dl.acm.org/doi/abs/10.1145/1323688.1323689).  

I would imagine that research in CC would aim to produce _general-purpose CC_ algorithms, akin to how numerical optimization research has produced optimization algorithms for broad classes of problems. Maybe these CC algorithms would employ human-like behaviors and strategies (finding disparate connections, exploring the boundaries and hidden assumptions of the problem), maybe not. But I haven't seen any work like this at CC conferences. This could be because I haven't read many CC papers.

[Open-ended search](https://www.springer.com/gp/book/9783319155234) seems very intriguing, yet I haven't seen it explored in the CC literature that I've looked at. Also, while Stanley and Lehman make very persuasive arguments that open-ended search isn't just optimization, operationalizing that seems extremely slippery. Nonetheless, I find it intriguing and have some vague research ideas based on it.







Should I just not worry about it?
=====

To some extent, you could say most of these things about AI research. None of the systems that we call "AI" are genuinely intelligent in any meaningful  sense, and genuine artificial intelligence seems nowhere on the horizon, though people debate this.  Yet, I do think we have algorithms that relate to aspects of human intelligence, and provide useful metaphors for human intelligence.

I also wish I had good places to submit papers related to artistic algorithms (when the papers aren't suitable for the big conferences), but I've been hestitant to submit to creativity conferences because I'm not sure I believe in their goals. 
Maybe I should just submit my NPR-ish papers to ICCC anyway, and ignore claims of CC, the way we mostly ignore claims of machine intelligence at AI conferences?

Even if I'm right that there's no such thing as CC, I expect that the CC community will still do worthwhile research, and build interesting systems.  

And I could be wrong–[I've backed the wrong horse before](http://www.dgp.toronto.edu/~hertzman/ibl2004/)–and maybe the CC community will make important discoveries. 