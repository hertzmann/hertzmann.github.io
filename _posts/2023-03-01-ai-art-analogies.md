---
layout: page
title: A Catalog of "AI" Art Analogies
summary:  "Is AI art more like photography, conceptual art, copying, image compression, recording music, or lava lamps?"
author:  AaronHertzmann
image: "/images/baldessari.jpg"
og:image: "/images/baldessari.jpg"

---

# A Catalog of "AI" Art Analogies

Since deep neural networks are hard-to-interpret mathematical functions, discussions and debate over "AI" art is partly expressed in analogies. Analogies are useful: they help us identify how the new thing might end up being similar to old things. [The ability to think with analogies may be the key to how humans have been able to collectively create entirely new things.](https://oneusefulthing.substack.com/p/blinded-by-analogies?utm_medium=reader2)
But they hide differences. All are useful in some ways, misleading in others.

The choice of analogy may reflect the speaker's agenda. Those of us who [compare it to photography](/2022/08/29/photography-history.html) emphasize its similarity to previous artistic technologies and movements that came to be accepted, but this has the danger of downplaying impacts on real peoples' careers.  People that say it's just direct copying argue that there's no value whatsoever in "AI" art.  Analogies sometimes serve as footsoldiers in the rhetorical battleground of social media.

In this post, I catalogue a few of the analogies for "AI" art and how they are useful analogies and how they're misleading.  [My previous blog post](/2022/12/17/when-tech-changes-art.html) delved into a few of these precedents in far more depth; read that post for a deeper analysis.


# [Photography](/2022/08/29/photography-history.html)
The most common analogy for computer-generated and procedural art, e.g., I used the analogy in [my  thesis back in 2001](https://mrl.cs.nyu.edu/publications/hertzmann-thesis/hertzmann-thesis-300dpi.pdf); I suspect many people come up with this analogy independently.  [There are many related analogies of technological shifts in art](/2022/12/17/when-tech-changes-art.html)

**How It's Useful**: 
Some of the most naive criticisms of "AI" art ("you just pushed a button!" "the machine did all the work!" "this will replace artists") were things that people said (and sometimes still say) about photography. If your criticism of "AI" also applies to photography, then maybe it's a naive criticism.

**The Subtext**: "AI" art is another tool for art, we just don't appreciate it yet. It will become an accepted, essential tool in our society, just as photography did.

**How It's Misleading**:
Disregards the role of training data, including the ethics of where the data came from and how data biases affects the outputs.


# Conceptual Art
Since artists like [Marcel Duchamp, Sol LeWitt, and John Baldessari](/2020/06/08/wica.html), contemporary art—and, especially, conceptual art—emphasizes the artist's initial idea, and not the execution. 

**How It's Useful**: Providing instructions to software is much like Sol LeWitt or John Baldessari providing instructions to a painter. Ideas about technical skill and craft being essential to art [are old-fashioned](/2022/09/27/art-eras.html).

**The Subtext**: Anything you do can be art, therefore "AI" art is art.

**How It's Misleading**: Most art in our world isn't conceptual art. Aesthetics, skill, and effort are important for most kinds of art that we care about.


<center>
<figure>
   <p float="left">
   <img src="../../../images/baldessari.jpg" alt="John Baldessari conceptual art" width="60%"/>
</p>
  <figcaption align="center"><i>Conceptual art by John Baldessari, in which he hired another painter to paint a picture.</i></figcaption>
</figure>
</center>


# Copying
Many recent critics of text-to-image call it copying, going so far as to say that these algorithms store databases of pictures on the web and use them at run-time to produce new images.


**How It's Useful**: [A few recent preprints have demonstrated cases](https://arxiv.org/abs/2301.13188) where some models can reproduce training images.

**The Subtext**: "AI" art is not art, it's dishonest and unoriginal.

**How It's Misleading**: 
This analogy is so wrong that it's hard to imagine how anyone came up with it in good faith.  These models do not store copies at test-time. So far, the instances when they duplicate training data seem to be quite rare and amenable to mitigation, e.g., they are cases with extensive training dataset duplication. More research is needed to fully understand these issues, but to say that it's "just copying" is simply wrong. 


# Theft
Critics of text-to-image say that it's theft.

**How It's Useful**: It could unjustly deprive people of income.

**The Subtext**: "AI" art is unethical and immoral.

**How It's Misleading**: "Theft" implies taking a physical object, like breaking into your home and taking a painting, or removing digital assets, like draining a bank account. Copying an image file is very different: if I copy your JPEG, you still have the JPEG.  [Unlike physical ownership, copyright law is not absolute ownership, and expanding copyright further could be harmful for artists and society](https://pluralistic.net/2023/02/09/ai-monkeys-paw/#bullied-schoolkids).

<center>
<a href="https://knowyourmeme.com/memes/piracy-its-a-crime"><img src="../../../images/piracy.jpg" alt="You Wouldn't Download A Car graphic"></a>
</center>



# Appropriation

Appropriation refers to at least two distinct, complex concepts: appropriation art (a form of conceptual art), and cultural appropriation. I haven't actually heard these analogies made much, but I think they're interesting.

**How It's Useful**: Both Appropriation Art and Cultural Appropriation are complex, difficult topics. Sometimes they're ok and sometimes they're not (e.g., Sherry Levine vs. Richard Prince), and there's no simple rules about which, and no consensus either. But, in both contexts, they signify, on one that, the benefits of cultural mixings and remix, and, on the other, thinking about systematic cultural harms to a class of individuals that can't easily be reduced to a simple formula.

**The Subtext**: It's complicated.

**How It's Misleading**: The fact that it's hard to draw a line about what's "ok" or "not ok" is sometimes taken to mean that you shouldn't try. Or that nothing is "ok." Unfortunately, the concept of cultural appropriation has been reduced to caricature, making it easier for people to dismiss.




# How Humans Learn to Make Art
Advocates say that training models from data is "just like" how humans learn to make art and to get inspired from other art.


**How It's Useful**:
We often underestimate the role of influence and inspiration on art, and the way that [everything is a remix](https://www.everythingisaremix.info/watch-the-series). All art is based on other art in some way; [people learn by imitation and copying](https://journals.sagepub.com/doi/full/10.1177/1354067X13515936); Homer, Shakespeare, and Van Gogh were all working from specific traditions and building from previous examples, specific to their times and places; the idea of the genius artist that invents everything from scratch is a myth.  

**The Subtext**: Training a model on data is a completely valid thing to do.

**How It's Misleading**:
To say that an "AI" algorithm works "just like" how a person does is wrong and misleading. [Computers are not people, and humans are not CPUs.](/2022/09/04/computationalism.html) We are not explainable by algorithms, and we have a higher moral status than machines. Even the term [machine learning is misleading](https://arxiv.org/abs/2104.12871) when it leads people to equate ML with human learning.  To say that "it's just like how humans learn" dismisses legitimate concerns with the ways these algorithms process data—and, besides, there are limits on when it's ok for humans to copy.


# Sampling and Collage

In music, sampling involves taking bits of pieces of sounds and reusing them in new ways, from musique concrète to hip-hop and beyond. In visual art, collage and photomontage involves cutting out photos and putting them together in new ways.

**How It's Useful**:
Remix in hip-hop and electronic music revealed to a lot of people how reusing existing elements can be transformative and create new art forms.

**The Subtext**: "AI" art is transformative, therefore it is a valid and legitimate artform.

**How It's Misleading**: 
Just as it's wrong to say these models are just copying the training data, it's probably wrong to say that they're copying bits and pieces of them in most cases. But it might be less wrong (or less-often wrong). Again, more research and study is needed here. The way these results are generated are often quite different from hip-hop sampling in lots of ways, for one thing the context is quite different. 


# Music Recording

At a few times in the 1920s and the 1930s, [musicians unions fought against the introduction of recorded music](https://www.smithsonianmag.com/history/musicians-wage-war-against-evil-robots-92702721/), including an advertising campaign against "robots" that seems eerily familiar today.

**How It's Useful**: It's a previous example of technological disruptions to art and employment, changing the availability of jobs but creating a tool that most of us take for granted. Musician unions were able to advocate for some protections for their members in spite of change.

**The Subtext**: Technological change happens, get over it.

**How It's Misleading**: Music recording is, first and foremost, about distribution platforms, although it enabled new kinds of art  as well (e.g., AOR). The role of distribution platforms (like streaming) is a related but somewhat different topic, and one that arguably has bigger implications for creators.



<center>
<figure>
   <p float="left">
   <img src="../../../images/cinemahistory/robot_sings_of_love.jpg" alt="1930 advertisement against recorded music in cinemas: the robot sings of love" width="60%"/>
</p>
</figure>
</center>



# Lava Lamp

In the past week, two high-profile art critics called an AI artworks a "lava lamp," ([Ben Davis](https://news.artnet.com/art-world/refik-anadol-unsupervised-moma-2242329), [Jerry Saltz](https://www.vulture.com/article/jerry-saltz-moma-refik-anadol-unsupervised.html)), and [a third used the term for AI art in general](https://www.newyorker.com/culture/cultural-comment/what-can-ai-art-teach-us-about-the-real-thing).

**How It's Useful**: Illustrates how something can be visually dazzling but otherwise hollow of meaning or significance.

**The Not-So-Subtext**: This stuff is just gimmicky eye-candy.

**How It's Misleading**: Dismisses the value of [experimentation](/2022/10/11/amateurs.html), form, and the many great things that have already been created with these techniques. 


# [Parrots](https://dl.acm.org/doi/10.1145/3442188.3445922)

Large Language Models (LLMs) are not sentient or intelligent, they are trained to produce high-probability sequences of text similar to a training corpus, like a parrot repeating things it has heard, without understanding.

**How It's Useful**: Deflates the wrong, misleading notions of AI sentience and intelligence.

**The Not-So-Subtext**: These things are convincing nonsense generators.

**How It's Misleading**: It doesn't quite ring true, because parrots repeats words or phrases, but you couldn't ask them to, say, generate an essay.  LLMs are much richer models than just repeating sentences.


# A Blurry JPEG

[Ted Chiang wrote an article entitled "ChatGPT Is a Blurry JPEG of the Web"](https://www.newyorker.com/tech/annals-of-technology/chatgpt-is-a-blurry-jpeg-of-the-web).

**How It's Useful**: Conveys the important concept that the model is lossily fitting and encoding a dataset.

**The Subtext**: It's regurgitating the data.

**How It's Misleading**: Like many of these analogies, it suggests these things are _just_ memorizing or collaging the data, rather than forming new, plausible combinations of it. 