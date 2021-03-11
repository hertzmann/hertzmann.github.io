---
layout: page
title: The Life-Cycle of AI Art
summary: How AI art evolves from technology to creativity
author:  AaronHertzmann
image: /images/vadim.jpg
---



# The Life-Cycle of AI Art

A fascinating new cycle for AI art techniques is emerging. I've alluded to this process in [previous papers](https://cacm.acm.org/magazines/2020/5/244330-computers-do-not-make-art-people-do/fulltext), but now that we're seeing this cycle repeat over and over, it seems possible to describe it more concretely.

Because of Twitter and GitHub repos, we have a sort of worldwide collaboration of artists and technologists happening, at an extraordinary pace. While there is a long history of artists and technologists collaboratting, and of individuals who innovate in both art and science simultaneously, this distributed international collaboration is—dare I say—_completely unprecedented_.

Some of the most significant AI algorithms that have fed this cycle are: DeepDream, StyleGAN, pix2pix, CycleGAN, BigGAN, and now DALL-E and CLIP.

The phases in this cycle seem to be:

1. **Computer science researchers release image generation code** on GitHub, usually accompanying a technical paper posted to arXiv or published at a conference.  Sometimes these papers say little or nothing explicit about making art; they are focused on technical and algorithmic problems, even though the paper figures are often inspiring or delightful. 

   We researchers share our papers and code online simply as part of the technical publication process, to allow other researchers to understand and reproduce our work.   There are some major downsides to the way this research has been conducted, but we can all agree that it has enabled technical development at a truly staggering pace, which have led to rapid development of new ideas in digital art.


2. **The links get widely shared on Twitter,** sometimes together with news articles and press releases about the technology.  Sometimes the release is more stealthy, only announced via the arXiv daily digest. One major route for dissemination are tweets by [AK](https://twitter.com/ak92501), who frequently Tweets highlights of the daily digest to  16K followers. 


3. **Artists and other tinkerers download the code and experiment with the technology,** kicking its tires, experimenting with different ways to use the technology to make images.  These are tech-savvy artists, skilled in coding with the ML tools, and generally willing to play in the mud. These artists sometimes post their first experiments _within days_ of the ML code release.  They share their results with each other on Twitter and share information and ideas with each other; most likely, they are also noticing which images get the most Likes and comments.     


    A lot of these experiments are whimsical, playing around, and play is an important part of exploration.  
  For example, [here's a review of Mario Klingemann's feed of BigGAN experiments](https://hyperallergic.com/481969/an-ai-artists-twitter-feed-is-an-art-gallery/)

    [How DeepDream's inspiring peculiarities arose from its research history](/2020/12/29/deepdream.html) is an instructive example of how seemingly-unimportant decisions made by researchers affect the artwork later on. 

     Only a handful of research papers get this attention from artists. And some, like GauGAN, see a lot of experimentation, but don't move past the experimentation phase much.


4. **Artists begin to release new work that uses these tools, showing it in galleries and exhibitions.** DeepDream, StyleGAN, and BigGAN have all been used in fine art exhibitions. DALL-E and CLIP are so new that they haven't yet, but it's only a matter of time.

5. **Enough artists use these tools in straightforward ways that the style of the technology becomes recognizable and predictable.** DeepDream was briefly amazing and then became boring pretty fast. GANs are a much richer space, but there is a lot of GAN-based art out there that all looks the same, and, I for one have lost interest in much of it. [GAN fatigue](https://www.mitpressjournals.org/doi/abs/10.1162/leon_a_01930) has set in.  However, most of the world hasn't seen GAN art, so there is still a considerable potential audience for it.

6. **The technology either matures or fades away.** 
I'm still enjoying Helena Sarin and Sofia Crespo's latest experiments with GANs, which are far more interesting than vanilla GAN renderings. 

7. **Then, eventually, some exciting new algorithm is released** and we go back to step one.

But even when methods fade away, they aren't gone. 
**The process is cumulative, and newer experiments mix-and-match ideas from newer and older ideas.**  Even though the cycle seems to be largely over for BigGAN and StyleGAN, the collective knowledge of these tools remains. For example, when CLIP was released, artists began to play with combining CLIP and BigGAN. 

[AI artists are generative artists, and writing code to make art—whether with AI algorithms or not—is a 60-year-old practice.](https://www.artnews.com/art-in-america/features/generative-art-tools-flash-processing-neural-networks-1202674657/). And more AI algorithms mean more paints in the paintbox of generative art.

Here are some other combinations of tools that were just shared in the past few days:

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">neuron #2478 &quot;surprised&quot;<br>exported to CPPN then GLSL and slightly animated <a href="https://t.co/j7kyURlxkc">https://t.co/j7kyURlxkc</a><br>NB: 13k parameters, may crash some GPU<br>[wtf twitter doesn&#39;t show shadertoy previews !?]<br><br>original technique by <a href="https://twitter.com/wxswxs?ref_src=twsrc%5Etfw">@wxswxs</a><a href="https://t.co/zYbLtHpXvk">https://t.co/zYbLtHpXvk</a> <a href="https://t.co/HWTRt9BAJI">pic.twitter.com/HWTRt9BAJI</a></p>&mdash; vadim epstein (@eps696) <a href="https://twitter.com/eps696/status/1369460655846264835?ref_src=twsrc%5Etfw">March 10, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Okay, now I&#39;m just being silly. Seriously. <a href="https://t.co/NMrhBzL8kV">pic.twitter.com/NMrhBzL8kV</a></p>&mdash; Doron Adler (@Norod78) <a href="https://twitter.com/Norod78/status/1369546359695630337?ref_src=twsrc%5Etfw">March 10, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

**There's lots of great stuff that happens outside this cycle.** For example, work by Tom White and Trevor Paglen doesn't really fit this pattern, who are  using AI technology in very different ways that don't follow this cycle.

Watching new forms of art develop is wonderful, and it's happening now, live, on social media, arXiv, GitHub, and beyond.