---
layout: page
title: "Occluding Contour Breakthroughs, Part 2: Getting It Right"
author:  AaronHertzmann
summary: New insight into line rendering algorithms
image: "/images/howtodraw/quadratic-patch.png"
og:image: "/images/howtodraw/quadratic-patch.png"
---


# Occluding Contour Breakthroughs, Part 2: Getting It Right


In the [first post in this series](/2023/07/31/occluding-contours-part-1.html), I outlined the problem of occluding contours for smooth surfaces, that we've never really fully understood. In this post, I'll explain our new insights that finally explain these long-standing problems, from this paper:

* Chenxi Liu, Pierre Bénard, Aaron Hertzmann, Shayan Hoshyari. _**ConTesse: Accurate Occluding Contours for Subdivision Surfaces.**_ ACM Transactions on Graphics (TOG). 2023. Volume 42, Number 1, Article No. 5. \[[paper webpage](https://dgp.toronto.edu/~hertzman/contesse/)\]

And then I'll discuss our even-newer approach:

* Ryan Capouellez, Jiacheng Dai, Aaron Hertzmann, Denis Zorin. _**Algebraic Smooth Occluding Contours**_. Proceedings of SIGGRAPH 2023. \[[paper webpage](http://ryanjcapouellez.com/papers/algebraic_smooth_occluding_contours.html)\]



# When Are Curves _Valid_?

Let's begin with a simple case: smooth objects for which the contour is a single, closed curve. For smooth surfaces, we can't compute the exact contour, so instead, we typically approximate it with a polyline in 3D. But how do we compute visbility of the polyline in a sensible way, [since the polyline isn't the contour of the surface](https://onlinelibrary.wiley.com/doi/10.1111/j.1467-8659.2008.01258.x)? We need to define a new triangle mesh for which the polyline is its contour.

The core idea we propose is that:

|A closed contour curve in the 2D image is _valid_ if and only if there exists a 3D surface for which this curve is the occluding contour.|

If a curve is valid, then there's a meaningful visibility assignment for it, using standard mesh visibility.

For example, this simple loop is _valid_ because it's the projection of a polyhedron's contours:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/mesh-contour-def.png" alt="Defintion of mesh occluding contours" width="80%"/>
</p>
</figure>
</center>
The same notion of validity applies both to smooth surfaces with smooth contours, and to polygon meshes with polyline contours.
I am being a bit hand-wavy about precise definitions here, in the interest of brevity; things are more precise [in our paper](https://dgp.toronto.edu/~hertzman/contesse/).

A valid contour loop might intersect itself in 2D, if the surface overlaps itself in image space:

<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/gamma-camera.png" alt="Smooth self-overlapping object in camera view" width="20%"/>
<img src="../../../images/howtodraw/gamma-side.png" alt="Smooth self-overlapping object in side view" width="20%"/>
</p>
</figure>
</center>
Here's a valid 2D polygon approximating this contour:
<center>
<figure>
<img src="../../../images/howtodraw/gamma-polygon.png" alt="Smooth self-overlapping object, polygonal approximation" width="20%"/>
</figure>
</center>
and, once we compute visibility, the rendering would look something like this:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/gamma_vis.jpg" alt="Smooth self-overlapping object, polygonal approximation with visibility" width="20%"/>
</p>
</figure>
</center>

# Invalid Polygons

Here's a contour polygon that's _invalid_:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/bowtie.png" alt="Bowtie polygon" width="30%"/>
</p>
</figure>
</center>
This is a single, self-intersecting polygon in a figure-8 configuration. I've drawn the vertices here; there is no vertex at the self-intersection point.   This polygon _cannot_ be the contour of a mesh: **There does not exist an orientable triangle mesh for which the occluding contour projects to this polygon,** with each polygon edge being the projection of one mesh edge.  

Hence, there's no "correct" way to determine visibility for this curve.

(One way to see this is to try to attach triangles that satisfy the constraint that contour edges connect front-faces to back-faces, and non-contour edges connect same-orientation faces. This constraint can't be satisfied because the contour is one-sided, like a Möbius strip. However, "two-sidedness" isn't a sufficient condition for validity.)

(In fact, there's no way to triangulate the above polygon that fills it with consistently oriented triangles. This is a broader notion of _validity_, and the one we actually use: any closed polygon is _valid_ if and only if it could be the projection of the boundary of a patch of 3D triangles that are all front-faces or all back-faces. )

So, there exist invalid polygons. Where do they come from? And how can we tell if a curve _is_ valid?


# Invalid Contours come from sampling

When do invalid contours occur? Well, suppose the actual smooth contour looks like this in 2D:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/invalid-source.png" alt="Curved object with smooth feature" width="30%"/>
</p>
</figure>
</center>
If you discretize it, you might get the figure-8 configuration:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/invalid.png" alt="Discretization with bowtie structure" width="30%"/>
</p>
</figure>
</center>
It's an invalid polygon, and now your visibility is busted.  

In a nutshell, this the fundamental problem: **All contour algorithms for smooth surfaces discretize the contours into polylines. This odiscretization often produces invalid polygons.** And invalid polygons do not have meaningful visibility. Sometimes it doesn't matter, because the invalid polygons are entirely hidden by occluders. But, eventually, all existing algorithms are going to produce visible errors due to invalid curves.  

This is an instance of the common-but-surprising fact that discretizing a continuous system does not preserve its properties, e.g., discretization breaks [some differential geometric properties on smooth surfaces](https://en.wikipedia.org/wiki/Discrete_differential_geometry), and breaks some conservation laws and collision handling in physical simulation.   

Unfortunately, it's not just figure-8 configurations; there are lots of ways that a polygon can be invalid.

# Theory

How can we determine algorithmically whether a curve is valid or not?

First, note that _linear projection preserves triangle orientation_. For example, if you project a front-facing triangle to image space, you get a triangle with positive orientation (i.e., `det([x1,y1,1;x2,y2,1;x3,y3,1])>0`). Curve orientation is also preserved. 

Let's look again at this example:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/mesh-contour-def.png" alt="Mesh contour definition" width="80%"/>
</p>
</figure>
</center>
The 3D contour bounds a set of front faces. These triangles project to a 2D collection of positively-oriented triangles, bounded by a 2D polygon.  They constitute a triangulation of the polygon.  This is the case for any valid hole-free collection of front-faces, even if the triangles self-overlap in image space.  

So, _for a 2D polygon to be valid, it must be possible to triangulate it with positively-oriented triangles_.  

How can we check if a polyline is valid?  Fortunately, there's a [dynamic programming algorithm from computational geometry](https://dl.acm.org/doi/abs/10.1145/73833.73838) to check this.  Specifically, the class of polygons I've discussed so far is called "self-overlapping."

Things get more complicated for typical surfaces: contours may have cusps, and collections of front-faces may have holes. These cases are discussed [in our paper](https://dgp.toronto.edu/~hertzman/contesse/).


# The ConTesse approach

So how can we deal with invalid polygons?  In the example above, we can simply refine the discretization, and stop when the curve becomes valid, e.g.,:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/invalid-subsampled.png" alt="Refined invalid configuration" width="30%"/>
</p>
</figure>
</center>

In our [paper](https://dgp.toronto.edu/~hertzman/contesse/), we begin with a subdivision surface, and discretize it into a mesh, including vertices sampled on the subdivision surface's contour. We check if all mesh contours are valid. If not, we insert more contour vertices, and check again. This is guaranteed to converge to valid contours, because the smooth surface's contours must be valid.

Then, we generate a new 3D mesh with contours that are both valid, and topologically-equivalent to the input surface's contours:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/fertility.png" alt="Example of our method on the Fertility model" width="90%"/>
</p>
</figure>
</center>


As far as I know, our method is the first that really solves the smooth contour visibility problem, guaranteeing valid curves if you run it long enough. 

However, making it work for entire surfaces is _far_ more involved than I've described here; see the paper for the full story.



# Hindsights

Ultimately, I view the ConTesse paper as a theoretical contribution together with an algorithmic proof-of-concept. It suggests future algorithms that are much more practical and efficient; there's also room to refine the theory.  Even when we were developing it we came up with better versions, but knew that we would never finish the project if we pursued them. See our Discussion section for much more on these topics.

This line of work began in [our 2014 paper](https://www.labri.fr/perso/pbenard/publications/contours/), which produced the idea that we should look for a valid mesh that preserves a smooth surface's contours (but not a reliable way to find it). That paper took five years from start to finish, with many, many false starts. It's amazing how these long, multiyear research efforts ultimately lead to ideas that seem so obvious and simple in retrospect.

I also want to acknowledge the extraordinarily hard work and insight that Chenxi brought to this paper under difficult pandemic conditions, as we stumbled through figuring out the theory and algorithms together. 

We can also look back and ask: do any historical algorithms guarantee validity?  In fact, I _think_ some do (although I'm not 100% sure). Specifically some of the Planar Map methods—[Winkenbach and Salesin's 1998 paper](https://dl.acm.org/doi/10.1145/237170.237287) and [Stroila et al.'s 2007 paper](https://ieeexplore.ieee.org/document/4359481/)—should give consistent contour visibility.  For example, Stroila et al. sample contour polylines  and then throw these polylines into a planar map library that (I believe) will break up any invalid polygons into valid pieces.
So they might produce lots of extra little bits of geometry, but they will all be valid. (The paper mentions that they remove tiny regions.) 

But some planar map algorithms don't produce valid visibility, like the [2011 algorithm of Karsch and Hart](https://dl.acm.org/doi/10.1145/2024676.2024683), which computes a planar map, but doesn't compute visibility according to a single consistent representation.  

Without our new theory, it was hard to know which of these methods were guaranteed to work and which suffered the same pitfalls as other contour methods.


# Piecewise Quadratic Surfaces

The problems created by sampling contours into polylines led us to the question: can we construct useful smooth surfaces where the contours _do_ have closed-form expressions?  In our new [SIGGRAPH 2023 paper](http://ryanjcapouellez.com/papers/algebraic_smooth_occluding_contours.html) with Ryan Cappouellez, Jiacheng Dai, and Denis Zorin, we found that the the answer is Yes.

Let's consider a single parametric patch **p**(_u_,_v_):

<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/quadratic-patch.png" alt="Patch parameterization" width="50%"/>
</p>
</figure>
</center>

The surface normal at a point is **n**(_u_,_v_) = **p**<sub>_u_</sub> x **p**<sub>_v_</sub>. 
Moreover, for now, let's assume we're using orthographic projection with a constant view vector **τ**.  Then, the contour is the set of points where _f_(_u_,_v_)=**τ** • **n**(_u_,_v_) = 0. 

If _f_ is quadratic, then we get a parametric contour: specifically, a conic section in (_u_,_v_).
And, we can make _f_ quadratic by choosing **p**(_u_,_v_) to be quadratic. This is the sweet spot: higher-order patches don't give parametric contours (except in some weird special cases), and lower-order is just a triangle. There's no other general-purpose algebraic solution possible.  

In order to model more general surfaces, we need to concatenate quadratic patches. In order for the contour to be continuous across patches, the boundaries need G<sup>1</sup> continuity; there may still be cusps at boundaries.

In the paper, we describe a novel G<sup>1</sup> piecewise quadratic construction to approximate an input mesh. The contours can then computed analytically as piecewise rational functions, and the remaining visibility operations involve fast numerical root-finding steps. See the paper for details.

Given a 3D mesh viewed under perspective projection, we first apply a projective transformation to the vertices, i.e., convert to camera coordinates, so that we're using orthographic projection.  

This method avoids all the complexity of finding valid polyline approximations, and we get these nice, clean contour extractions:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/quadratic-fertility.png" alt="Example of quadratic algorithm" width="90%"/>
</p>
</figure>
</center>
Moreover, it's much faster than ConTesse. It takes at most one second per frame at run-time for most of the meshes we tested.

Once you have these contours, you can stylized them cleanly:
<center>
<figure>
   <p float="left">
<img src="../../../images/howtodraw/spot-model.jpg" alt="Spot model" width="40%"/>
<img src="../../../images/howtodraw/spot-stylized.jpg" alt="Spot model" width="40%"/>
</p>
</figure>
</center>

And, our method works robustly for every point of view, no more random, unpredictable gaps in the results:
<center>
<video width="640" height="480" controls>
  <source src="../../../images/howtodraw/spot_contours.mp4" type="video/mp4">
Your browser does not support the video tag.
</video></center>



**I believe this represents the state-of-the-art for efficiently producing smooth, sensible occluding contours from a triangle mesh.** And, even if you're starting with a subdivision surface, depending on your needs, your best bet may be to turn it into a triangle mesh and then run our algorithm.





# Next Steps

[In part 3](/2023/07/31/occluding-contours-part-3.html), I'll summarize which methods I think are best for which problems, and where the open research problems are.