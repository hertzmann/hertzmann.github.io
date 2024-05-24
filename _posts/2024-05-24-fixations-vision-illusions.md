---
layout: page
title: "Visual Illusions Explainable by the Limitations of Peripheral Vision"
summary: Illusions that reveal the role of eye fixations for pictures
author: AaronHertzmann
image: "/images/illusions/ranso-entangle01.jpg"
og:image: "/images/illusions/ranso-entangle01.jpg"
---

# Visual Illusions Explainable by the Limitations of Peripheral Vision

What happens when you look at a picture? Your eyes move over the picture, to take in different parts of it.  In each eye _fixation_ on a picture, we get a sense of part of a picture, and piece those different parts together in some way. Most of the time, we don't really think about these eye movements and the role they play.

But something complicated is happening in the way we connect these fixations. This blog post describes a set of [visual illusions (a.k.a. optical illusions)](https://en.wikipedia.org/wiki/Optical_illusion) that reveal these complications.  

All of these examples create illusory impressions of change when you move your eyes from one part to another. They do this by giving you a very different impression of a part of the picture when you like right at it, versus when you look to the side. It's very weird for part of a still image to look different depending on where you fixate.

**I hypothesize that these phenomena can be explained by peripheral visual encodings,** which I'll explain below. These illusions demonstrate the importance of peripheral vision in perceiving pictures, and what happens when peripheral vision get "confused," and how it does. 

My [previous blog post](/2024/05/09/illusion-of-awareness.html) discussed how these same concepts around peripheral vision explain real-world illusions of awareness.



# The Cafe Wall Illusion

Here's a pattern in which the lines look curved and tilted:

<center>
	<a href="../../../images/illusions/cafe_wall.png"><img src="../../../images/illusions/cafe_wall.png" width="480"></a>
</center>

Yet, if you search over the image, you won't find any individual lines that are curved or tilted.

This is callled the [Cafe Wall illusion](https://en.wikipedia.org/wiki/Caf%C3%A9_wall_illusion), and was first described by 19th-Century psychologist. It gets its name from the pattern of tiles on the wall of a cafe.

Here's the same picture, but with lower-contrast tiles, to demonstrate that the lines are actually straight:

<center>
	<a href="../../../images/illusions/cafe_wall_nocontrast.png">
	<img src="../../../images/illusions/cafe_wall_nocontrast.png"  width="480"></a>
</center>

Here's the key thing to notice, when looking at the cafe wall illusion. When you fixate your eyes on any specific part of the picture, the lines look straight and axis-aligned (either horizontal or vertical). But, off to the side, the lines look curving and tilting. Then, when you move your eyes, everything seems to shift: now the new lines you're fixating on are straight and axis-aligned, and the part you were just looking at is curved and tilting.  It's as if the picture happened to change exactly when you moved your eyes.  This kind of visual contradiction doesn't happen in normal pictures,


# The Entangled Illusion and Eye Movements

Here are two concentric rings that do not look like concentric rings:

<center>
	<figure>
		<a href="../../../images/illusions/ranso-entangle01.jpg">
		<img src="../../../images/illusions/ranso-entangle01.jpg" width="480"></a>
	</figure>
	<figcaption><i><a href="https://www.psy.ritsumei.ac.jp/akitaoka/uzu10e.html">"Entanglement illusion" by Akiyoshi Kitaoka</a></i></figcaption>
</center>

Somehow they seem connected, yet, in each point you fixate on, they appear as two separate rings. You can trace your eyes or finger around the space between the circles to confirm it.

Here, the difference between the parts you fixate, and the parts off to the side, is substantial, almost like they're different pictures. There are two separate rings where you fixate, but they seem connected somehow off to the side. But, if you move your eyes, the roles shift.



# What's going on: peripheral visual encoding

Although we see a wide field-of-view from each eye, we see fine detail only in a narrow range. For example, fixate your eye on any word and see how many other words nearby that you can read. Not very many. If you hold out your hand at arms' length, then the region where you get fine detail is, roughly, the size of your thumb (or maybe the width of five fingers, it doesn't matter), which is a tiny fraction all the things you see. 

Everything outside that thumb-width of whatever you're looking at is called _peripheral vision_. Peripheral vision doesn't give as much detail as the things we look right at. For this reason, scientists often talk about it as though it's just blurry vision. But it's more complicated than that.

For example, if you stare at the top **+**, then it should be easy to recognize the **V** to the left. However, if you stare at the bottom **+**, then the **V** is unrecognizable, even though it's the same size and distance from the **+**.
<center>
   <figure>
         <p float="left">
<img src="../../../images/awareness/xvk.jpg"/>
</p>
</figure>
</center>

This is because of the **peripheral visual encoding**: the brain doesn't just store a blurry picture of the light in peripheral vision, it summarizes it with statistical measurements. At this statistical encoding can mix things together, losing information about which letter is which when there are multiple letter.

I hypothesize that **for the illusions on this page, the fact that things look different when viewed directly, versus in peripheral vision, suggests that peripheral visual encodings cause the illusions.**

# Spatial metamer visualizations

It's not easy to understand or visualize peripheral visual encodings.  It seems that the brain is converting light measurements into a high-dimensional feature space of summary statistics, and these do not have easy visual interpretations.

Vision scientists visualize these encodings with  _spatial metamers_: pictures that have visually equivalent statistics to a given image, for a given fixation. That is, you pick an eye gaze location in a picture, and a metamer can be generated that jumbles up the image in a way that is not noticable when fixating on that location. These metamers illustrate that peripheral vision isn't just blurry vision.

Here is an example:
<center>
   <figure>
         <p float="left">
<img src="../../../images/awareness/bus-stop.jpg" width="30%"/>&nbsp;<img src="../../../images/awareness/bus-stop-metamer1.jpg" width="30%"/>&nbsp;<img src="../../../images/awareness/bus-stop-metamer1.jpg" width="30%"/>
</p>
   </figure>
   <figcaption><I>Figure from <a href="https://www.annualreviews.org/doi/abs/10.1146/annurev-vision-082114-035733">Rosenholtz (2020)</a></I></figcaption>
</center>
The middle and rightmost pictures are two spatial metamers of the left image. As long as the pictures are displayed large enough on your screen, then looking at the middle or rightmost picture should look the same as looking at the left picture, but only when looking at the center. 

In their edges, the metamers look jumbled up. The peripheral visual encoding, formed of statistical summaries, doesn't notice the jumble.

This video provides a compelling demonstration, at about 10 seconds in:
<center>   <figure>
<video controls width="600">
  <source src="https://dl.acm.org/action/downloadSupplement?doi=10.1145%2F3564605&file=tap-2021-0028-file001.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
<figcaption><i>Video accompanying <a href="https://dl.acm.org/doi/full/10.1145/3564605">Brown et al. (2023)</a> You might need to view in full-screen for the best results.</i></figcaption></figure>
</center>
If you follow the red dot closely, you shouldn't notice the picture changing at all. If you look away from the red dot, you can easily see the background change. 


# Metamer visualization of the illusions


Here's a metamer of the low-contrast cafe wall (generated using <a href="https://github.com/ProgramofComputerGraphics/PooledStatisticsMetamers">code from Brown et al.</a>):
<center>
   <figure>
         <p float="left">
<a href="../../../images/illusions/cafe_wall_nocontrast_gazemet.png">
   <img src="../../../images/illusions/cafe_wall_nocontrast_gazemet.png" width="480"/></a>
</p>
   </figure>
</center>
In principle, this picture should look the same as the original if you fixate on its center; although it doesn't work for me, this might be a failure case of the algorithm, or maybe I didn't blow it up large enough. Even so, the key thing to notice here is that the jumbled-up picture still has a lot of horizontal and vertical lines. It seems like preserving important peripheral statistics of this picture involves using horizontal and vertical lines. Even where there's some waviness, there's no clear "tilt" or orientation.

Here's a metamer of the original cafe wall illusion (with color removed):
<center>
   <figure>
         <p float="left">
         	<a href="../../../images/illusions/cafe_wall_gazemet1.png">
<img src="../../../images/illusions/cafe_wall_gazemet1.png" width="480"/></a>
</p>
   </figure>
</center>

Now, the image periphery includes more-tilted lines; it's most visible in the lower-left. In the upper-right, there seem to be more angled lines. So this effect is subtle, but I seems to support the hypothesis that the cafe wall creates peripheral encodings corresponding to tilted statistcs.  **While I don't think these metamers _prove_ anything, I think they support the interpretations I'm proposing.** 

Here's a metamer of the entanglement illusion:
<center>
   <figure>
         <p float="left">
         	<a href="../../../images/illusions/ranso_gazemet.png">
<img src="../../../images/illusions/ranso_gazemet.png" width="480"/></a>
</p>
   </figure>
</center>
Notice how the curves get broken up. But if we make the rings solid:
<center>
   <figure>
         <p float="left">
<a href="../../../images/illusions/ranso_solid.jpg">
<img src="../../../images/illusions/ranso_solid.jpg" width="480"/></a>
</p>
   </figure>
</center>
Then the metamer is solid as well:
<center>
   <figure>
         <p float="left">
<a href="../../../images/illusions/ranso_solid_gazemet.png">
<img src="../../../images/illusions/ranso_solid_gazemet.png" width="480"/>
</a>
</p>
   </figure>
</center>


# More Tilt Illusions

Similar effects occur in many other illusions. In each case, the illusory effect appears in peripheral vision, but not in fixations. The two seem to have contradictory appearances, and so the picture's appearance changes as you move your eyes.

A heuristic I follow here is: **if the visual impression you get fixating on a point contradicts the impression when the point is viewed from the side, then the illusion might be caused by peripheral encodings.** In the Cafe Wall illusion, points look rectinilinear when viewed directly and angled in peripheral vision.


**Fraser spiral.** The [Fraser Spiral](https://en.wikipedia.org/wiki/Fraser_spiral_illusion), created by a British psychologist in 1908, shows a more complex version of the same phtenomenon:
<center>
	<figure>
		<a href="../../../images/illusions/Fraser_spiral.png">
		<img src="../../../images/illusions/Fraser_spiral.png" width="480"></a>
	</figure>
</center>
This, too, consists of concentric circles, but it looks like a spiral.

In each case, any part that you fixate on looks circular, but the overall effect is of a spiral.  Confirming this is quite challenging, either by scanning your eyes over the pictures, or by moving your finger around it. Trying both is instructive, it suggests how peripheral vision may affect both eye movements and hand movements.

**Zollner's orientation illusion (1860).**
These, in turn, follow from a sequence of earlier illusions developed by 19th-century psychologists, including [Zollner's orientation illusion](https://en.wikipedia.org/wiki/Z%C3%B6llner_illusion) of 1860:
<center>
	<figure>
		<a href="../../../images/illusions/Zollner.png">
		<img src="../../../images/illusions/Zollner.png"></a>
	</figure>
</center>
The long straight lines are parallel, but they look angled in peripheral vision. 

Here are the same long lines, without the short ones:
<center>
	<figure>
		<a href="../../../images/illusions/Zollner_edited.png">
		<img src="../../../images/illusions/Zollner_edited.png"></a>
	</figure>
</center>
Now they do appear parallel.

**Hering**.  In the [Hering Illusion](https://en.wikipedia.org/wiki/Hering_illusion) of 1861, the two parallel lines are straight, but appear curved:
<center>
	<figure>
		<a href="../../../images/illusions/Hering.png">
		<img src="../../../images/illusions/Hering.png"></a>
	</figure>
</center>
If you fixate on the center of the picture, the red lines look curved. But, if you fixate on any part of the red lines, that part looks straight.





# Illusory peripheral motion

Here are some effects where illusory motion appears in peripheral vision, suggesting a peripheral encoding cause.

In the **[peripheral drift illusion](https://en.wikipedia.org/wiki/Peripheral_drift_illusion)**, objects appear to move when you move your eyes:
<center>
	<figure>
		<a href="../../../images/illusions/rotsnake.gif">
		<img src="../../../images/illusions/rotsnake.gif"></a>
	</figure>
	<figcaption><i><a href="https://www.ritsumei.ac.jp/~akitaoka/index-e.html">"Rotating Snakes" by Akiyoshi Kitaoka</a></i></figcaption>
</center>
Trying moving your eyes within one of the circles. Note that the circle you fixate on doesn't seem to rotate much, whereas the others do.

In the **[Pinna illusion](http://www.scholarpedia.org/article/Pinna_illusion)**, you fixate on the center of the picture, and then move your head closer to the picture (or move the picture closer to your head). The circles will appear to rotate.
<center>
	<figure>
		<a href="../../../images/illusions/pinna.jpeg">
		<img src="../../../images/illusions/pinna.jpeg" width="480"></a>
	</figure>
	<figcaption><i><a href="https://x.com/AkiyoshiKitaoka/status/1787988556767690956">"Pinna illusion" by Akiyoshi Kitaoka, based on illusion by Baingio Pinna</a></i></figcaption>
</center>

In the **Furrow Illusion,** the circles seem to be moving in different directions depending on whether you're looking right at them, or looking to the side:

<center>   <figure>
<video width="600" height="400" controls loop>
  <source src="../../../images/illusions/Furrow.mov" type="video/mp4">
Your browser does not support the video tag.
</video>
<figcaption><i><a href="https://jov.arvojournals.org/article.aspx?articleid=2191978">Furrow illusion by Stuart Anstis</a></i></figcaption></figure>
</center>

In the **Leviant Traffic illusion**, motion appears in the outer rings when you fixate on the center of this pattern (you might need to expand the picture to a large size by clicking on it):

<center>   <figure>
		<a href="../../../images/illusions/leviant.jpg"><img src="../../../images/illusions/leviant.jpg" width="480"></a>
<figcaption><i>Leviant Traffic illusion, <a href="https://www.frontiersin.org/articles/10.3389/fnhum.2022.875829/full">illustration by Christopher Tyler</a></i></figcaption></figure>
</center>

This is a version of the [**MacKay Chrysanthemum**](https://www.frontiersin.org/files/Articles/875829/fnhum-16-875829-HTML-r2/image_m/fnhum-16-875829-g010.jpg). 

A further extension is Tyler's [**Perceptual Tachyons**](https://www.frontiersin.org/articles/10.3389/fnhum.2022.875829/full). [This is a very striking and cool illusion that you can view here](https://www.dgp.toronto.edu/~hertzman/tachyons/).


# Grid illusions

[These grid illusions](https://en.wikipedia.org/wiki/Grid_illusion) seem to depend on fixations and peripheral vision. 

In the **Hermann grid** of 1870, dots appear at the corners depending on where you look:
<center>
	<figure>
		<a href="../../../images/illusions/HermannGrid.png">
		<img src="../../../images/illusions/HermannGrid.png"></a>
	</figure>
</center>

In the **Scintillating dots illusion** dots appear and disappear as you move your eyes:
<center>
	<figure>
		<a href="../../../images/illusions/Scintillating.png">
		<img src="../../../images/illusions/Scintillating.png"></a>
	</figure>
</center>
The rapid appearance and disappearance indicates that it cannot be due to static peripheral encodings, but it could be due to peripheral motion encodings.


# Illusions due to fragmentary awareness

Here are some visual illusions that, I think, are not due to peripheral visual encoding, but, just to the fact that we must move our eyes to interpret pictures, and we never seem to store the whole picture in our brains.  

So you're continually interpreting the current fixation in terms of an abstract notion of the surroundings. This works fine with the 3D scene or picture represents a consistent scene, but what about when the picture is impossible? For example, in impossible pictures, each fixation looks reasonable, but the overall shape doesn't add up:

<center>
	<figure>
		<img src="../../../images/illusions/Poiuyt.jpg" width="320">
	</figure>
</center>

If the impossibility is visible within a single fixation, then the picture is much less interesting:

<center>
	<figure>
		<img src="../../../images/illusions/Poiuyt-short-crop.jpg" width="60">
	</figure>
</center>

These things get more interesting when the picture looks more realistic:

<center>
	<figure>
		<img src="../../../images/illusions/triangle.jpg" width="320">
	</figure>
</center>
or more elaborate:
<center>
	<figure>
		<a href="../../../images/illusions/steinberg.png">
		<img src="../../../images/illusions/steinberg.png" width="480">
	</a>
		<figcaption><i><a href="https://saulsteinbergfoundation.org/artwork/drawing-in-the-new-yorker-november-30-1963/179-tny-11-30-63-lgr/">Saul Steinberg, 1963</a></i>
		</figcaption>
	</figure>
</center>



**Indeterminate pictures** also look beguiling, in that each fixation seems plausible, but it's never really clear whether or not they do add up to anything:

<center>
	<figure>
		<a href="../../../images/pepperell-impulse.jpg">
		<img src="../../../images/pepperell-impulse.jpg" width="480"></a>
	</figure>
	<figcaption><a href="https://www.frontiersin.org/articles/10.3389/fnhum.2011.00084/abstract">"Impulse," painted by Robert Pepperell, 2006</a>		
	</figcaption>	
</center>


Here's a different sort of fixation dependence:

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">A train appears to step. <a href="https://t.co/jJWn2HXImp">pic.twitter.com/jJWn2HXImp</a></p>&mdash; Akiyoshi Kitaoka (@AkiyoshiKitaoka) <a href="https://twitter.com/AkiyoshiKitaoka/status/1788904529121206438?ref_src=twsrc%5Etfw">May 10, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

The train appears to move, when it's standing still. But, if you fixate on the outline of the train, it's obviously not moving. If you could somehow process the entire shape simultaneously, rather than separately per-fixation, there would be no illusion of movement.


# Further reading

For discussion of how the illusion of awareness and peripheral vision, see [**my previous blog post**](/2024/05/09/illusion-of-awareness.html).

For more amazing illusions, see [Akiyoshi Kitaoka's illusion pages](https://www.ritsumei.ac.jp/~akitaoka/index-e.html), and, relevant to this post, his review of tilt illusions:

* Akiyoshi Kitaoka. [**Tilt illusions after Oyama (1960): A review**](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1468-5884.2007.00328.x). _Japanese Psychological Research_. 2007.

For discussion of peripheral vision, see:

* Ruth Rosenholtz. [**Capabilities and limitations of peripheral vision**](https://www.annualreviews.org/doi/abs/10.1146/annurev-vision-082114-035733). _Annual Review of Vision Science_, 2016.

To generate spatial metamers, I used code from this paper, which includes a good background discussion of metamer generatino:

* Rachel Brown, Vasha DuTell, Bruce Walter, Ruth Rosenholtz, Peter Shirley, Morgan McGuire, David Luebke. [**Efficient Dataflow Modeling of Peripheral Encoding in the Human Visual System.**](https://dl.acm.org/doi/full/10.1145/3564605) _ACM Trans. Applied Perception._ 2023.

For more discussion of how peripheral vision relates to realistic pictures and to impossible pictures, see:

* A. Hertzmann. Toward a Theory of Perspective Perception in Pictures. _Journal of Vision_. April 2024, 24(4). \[[Paper](https://jov.arvojournals.org/article.aspx?articleid=2793609)\] \[[Webpage](https://www.dgp.toronto.edu/~hertzman/perspective/)\] 


