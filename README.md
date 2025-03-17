# Stanford CS248A Final Projects

## Due dates

1. The project proposal is due __Wed, Feb 26th__ 11:59:59 PM, but feel __strongly encouraged__ to submit earlier to get quicker feedback.
2. Your final project demo video is due on __Monday, March 17th__ at 8 PM.
3. Your final project hand-in (writeup + code) is due on Tuesday __March 18th at 3:00pm__.
4. The project proposal deadline is "soft" in that we strongly encourage you to submit a proposal, but the proposal is not graded.  The purpose of the project proposal is to give you an opportunity to put your plans down on paper so you can get feedback from the staff about whether the project is too easy or too hard before it is too late. The writeup and video deadlines are hard deadlines --- __there are no late days__

__We will have a final project celebration and watch party to watch all the project videos as a group during our final exam slot on Tuesday March 18th from 3:30-5pm__. All on-campus students in the class is expected to come in person. We will give exemptions on a case-by-case basis.

## Summary

For the final assignment in this course you are free to design your own project. The only guidelines are as follows:

1. We love it when students get artistically creative with projects (we want to see some great final pictures and animations!), but a major portion of the assignment should be a technical component.  For example, creating a complex scene in 3D modeling package like [Blender](https://www.blender.org/) or implementing a mini-game in [Unity](https://unity.com/) via their level-editing tools is not a well-targeted final project for CS248A.  However, implementing a technique discussed in class in Unity would be a reasonable project.

2. Since the project spans approximately three weeks of the quarter (and that period of time includes an exam), our expectations are that you attempt a project that is approximately the scope of course programming assignment (perhaps a little bit more work if you have the time).  In creating your proposal we want to you design a project that is challenging, but can reasonably be done in three weeks.  __We encourage you to be ambitious, but keep in mind you likely have other course projects and obligations during this time as well.__

3. Just like with all course programming assignments, you can work in teams of up to two students.

4. A good template for a project would be to dream up an image or video you want to create and finding an example of that image/video. In your proposal show an image that you have in mind (e.g., download a photo, illustration, or someone else's computer-generated image) from the internet as an example to convey your goals. Once you have an image in mind, then all your project work can just be focused on implementing the algorithms necessary to create that image.

Please feel encouraged to discuss project ideas with your classmates and the staff on Ed or during office hours. To allow the staff to help you make sure your project is appropriately related to themes from the class and is appropriately scoped for the given amount of time, we ask you to submit a short project proposal. (see below for details).

## A Few Project Ideas ##

We will release example demo videos from a number of prior projects on Canvas/Panopto (the same place lecture videos are hosted).  We encourage you to take a look at what students have tried in the past.  However, you'll notice that some of these prior projects involved animation algorithms.  Animation was previously covered in CS248A, but has now been moved to CS248B.  I prefer that your projects focus on topics closer to what we learn about in CS248A, but if you are really, really interested in doing an animation project (the one documented on the Cardinal3D wiki), come talk to me.

You are encouraged to design your own project, but here are some examples to get you thinking:

* __Implicit Surface Rendering__:
  If you are interested in geometry, you can explore implicit surfaces through Signed Distance Fields. The way that your renderer from Assignment 3 computes intersections between a ray and geometry is by relying on the triangle primitives in meshes. Instead, you could imagine that geometry is described by equations rather than meshes with discrete points (think about the sphere example in Cardinal3D). A popular way to render implicit surfaces is through [Ray Marching](https://en.wikipedia.org/wiki/Ray_marching). See (https://iquilezles.org/articles/raymarchingdf/) for many examples of how powerful this technique is. A final project option is to write a ray marcher and implement SDFs for a few types of geometry. Then you can make a 3D scene out of your geometry primitives that can render very quickly!

* __Spatial Acceleration Data Structure__:
  In the Ray Tracing project, you implemented BVH building and traversal to speed up ray/scene intersection. Time to implement some more data structures! Implement two separate spatial acceleration data structures: we recommend an octree and a KD-tree. In production and game engine design, special care is taken when choosing which spatial acceleration data structure to use. Engineers have to consider the specific requirements of the scene and the advantages/disadvantages of each data structure. To that end, please research the advantages and disadvantages of each of your data structures (BVH + two more). Then, for each data structure, create one scene that showcases the data structure’s advantage, and one scene that showcases the data structure’s disadvantage. (You should have at least 6 scenes by the end.)

* __Volume Path Tracer__:
  Want to render clouds and smoke? These are “volumetric” objects that can be pathtraced just like the cubes and spheres in the Cornell Box. Extend your path tracer to support volumetric path tracing. Here are some resources to get you started:
  https://cs.dartmouth.edu/~wjarosz/publications/novak18monte-sig.html
  https://cseweb.ucsd.edu/~tzli/cse272/wi2023/homework2.pdf
  Then show us some of your beautiful renders of volumetrics!  Another reason to write a volume renderer is that volume rendering is easy to make differentiable, so you could write a volume renderer that is used to recover a 3D scene from photographs, like what's done in NeRF.

* __Stylized Shaders, Pixel Art Shaders__:
  In programming assignment 3, you learned how to raytrace photorealistic images of 3D scenes. Now, imagine you can render a 3D scene in a non-photorealistic way, with a specific art style. Stylized shaders can manipulate light, color, texture, and edge detection to achieve a look that resonates with particular artistic movements or personal aesthetics. They offer a versatile toolset for artists and developers to craft visuals that are expressive, mood-setting, and distinct from the conventional realism in 3D graphics.
  There are many shader styles you can implement. One of the most popular ones is the Toon/Cel Shader. You can read more about it on [Wikipedia](https://en.wikipedia.org/wiki/Cel_shading).

* __Texture Mapping in a ray tracer__
  Texture mapping is like giving your 3D objects a makeover with new skin, allowing you to wrap images around them so they look like they have intricate details – think wood grains on a table or the weave of fabric on a couch! Remember in drawSVG, we implemented texture mapping and were able to render an image element within a given SVG. Now, you can also implement texture mapping in your Programming Assignment 3 to jazz up your scene!
  You might also experiment with different mapping techniques such as UV mapping, procedural texturing, or bump mapping to simulate surface irregularities and give your objects a tactile feel. Pay special attention to texture resolution and filtering methods to avoid common pitfalls like pixelation or blurring, ensuring your textures look crisp and believable from all angles. Additionally, reflect on how textures can enhance the storytelling of your scene – use them to add character to objects, set the mood, or define the time of day.

The following are cool areas in graphics to draw from. Feel free to draw on these in your own proposals! You can pick portions of them to implement based on what you’ve learned in this class:

* __Stylization of Meshes__:
  Similar to non-photorealistic pixel shaders, we can render geometry in non-photorealistic ways! Check out this fun paper: [Cubic Stylization by Hsueh-Ti Derek Liu and Alec Jacobson](https://www.dgp.toronto.edu/projects/cubic-stylization/). Imagine you have a squishy toy that you can mold into a shape that's kind of like a cube, but still looks like the toy. That's what this paper’s 3D styling trick does with digital shapes. The authors found out that you can make shapes look more like cubes if you treat their surfaces like stiff paper that only folds at sharp angles, not like cloth that can bend smoothly. By adjusting how the surfaces of the shape fold, we can keep the important details while giving it that cubey look. Try this for a fun geometry project!

* __Neural Importance Sampling__:
  Can neural networks be used to help sample when ray tracing a scene? In class, we talked about different importance sampling techniques; in Neural Importance Sampling [Muller 19], authors describe a manner to fit neural networks to sample distributions in scenes. Check it out! http://jannovak.info/publications/NIS/index.html

* __Differentiable Rendering to Recover 3D Representations from Photos (NeRF and Gaussian Splatting)__:
  Radiance fields have become a popular topic in computer graphics and computer vision since the publication of [NeRF](https://www.matthewtancik.com/nerf) (Neural Radiance Fields). A more recent method with excellent results is [Gaussian Splatting](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/), which is based on decades-old graphics techniques. If you are interested in state-of-the-art computer vision or optimization, implementing a portion of Gaussian Splatting would be a great final project. “Splatting” has been around for the past 30 years, and refers to rendering by rasterizing point clouds onto an image plane. You’ve written a rasterizer :) Instead of a point cloud, gaussian splatting uses gaussians (picture a blurry point in 3D). It then optimizes over the set of gaussians to match different input images of the scene. The outputs are very cool synthesized views that make the 2D images appear to be 3D.

You can also choose to extend the programming assignments from this class:

* Extend the SVG renderer from Assignment 1 so it can render as many SVG files from the web as possible.  This would involve adding support for new primitive types: spline curves, elipses, rotated images, fonts, text. etc that you might not have had a chance to implement during Assignment 1.  We recommend that you start by downloading some interesting SVG's and then continue to add features to your SVG renderer until it correctly renders them. (You might have to improve the starter code's SVG parser to support these more advanced effects as well.)

* Extend the path tracer assignment with new features. This might include:
   * [Accurate camera simulation](https://graphics.stanford.edu/papers/camera/) or [motion blur](http://psgraphics.blogspot.com/2016/02/motion-blur-in-ray-tracer.html)
   * Support for ray tracing new primitive types, like [subdivision surfaces](https://graphics.stanford.edu/~boulos/papers/subdiv_tr.pdf).
   * Extend your renderer to do multi-spectral rendering, where you trace different rays for different wavelengths, allowing you to render prism-like effects [like this] (https://blender.stackexchange.com/questions/1602/light-spectrum-dispersion-effect-in-blender).  This involves changing the `Spectrum` class to support more color channels and also modeling wavelength-dependent refraction.
   * Add important-sampled environment maps to your ray tracer. How do you importance sample environment maps?

* __Shaders__: This is a past assignment from this class. You are given a simple real-time renderer and a simple 3D scene. However, the starter code implements only very simple material and lighting models, so rendered images do not look particularly great.  You will improve the quality of the rendering by implementing a number of lighting and material shading effects using the GLSL, OpenGL's [shading language](https://thebookofshaders.com/01/), as well as some OpenGL client code in C++. Through this project option the point is to get basic experience with modern shader programming, and to build understanding of how material pattern logic, material BRDFs, and lighting computations are combined in a shader to compute surface reflectance. There are countless ways you can keep going by adding more complex materials and lighting.
  Starter Code: https://github.com/stanford-cs248/shading

* __If you are interested in performance__, take your Assignment 1 or Assignment 3 path tracer any parallelize it onto multiple cores and even using SIMD instructions. (We recommend using [ISPC](https://ispc.github.io/) for generating SIMD code for a CPU. Ray tracing is aready parallelized across cores, but it would be interesting to consider SIMD ray tracing and multi-core parallel BVH construction.

* In the past, some students have done projects involving Apple's [AR-Kit](https://developer.apple.com/augmented-reality/).

* If you are interested in real-time 3D graphics engine programming, write a 3D renderer from scratch using a modern GPU-accelerated grapshics API like Direct 12 or Vulkan.

* A big idea these days is using machine learning to determine how to combine a small number of supersamples into a final high quality resolved result.  The result is that images produced with only a small number of samples per pixel look as it they were rendered with much higher sample counts. See techniques like [morphological anti-aliasing](http://www.iryoku.com/mlaa/), which predated use of modern deep learning techniques, or more modern techniques based on DNNs for image-to-image transfer (called in DLSS by NVIDIA).

* Implement corners and creases in Catmull-Clark subdivision. (This on its own is a little small for a project, it might be part of a project that also includes additional extra credits from Assignment 2.)


## The Project Proposal ##

Please submit a proposal via Gradescope. Your proposal can be short (2 pages max), but it should clearly state your plans for the project.  If you submit prior to March 3rd, please let the staff know on Ed so they can give you feedback early.  Please follow the guidelines/template below:

The proposal will have the following sections:

* __Project Title:__  A great title is catchy, but also descriptive!

* __Names and SuNET ID's__ of the people working on the project

* __Summary:__ A brief 2-3 sentence summary of your project goals plus a potential image or link to a video that shows off an example of something you'd like to create. For example: _"We are going to extend assignment 1 with support for drawing spline curves so that we can render SVGs with curves and arbitrary True-Type fonts. We want to be able to render an image that looks like..."._  or _"We are going to extend assignment 2 with support for mesh downsampling via the quadratic error metric.  We will use this implementation to generate meshes of various levels of detail that we will import into Unity and show how we can choose the right mesh to render as a character gets closer and farther from the camera on screen."_

* __Task list:__ No more than a few paragraphs of description of what you will do.  Most importantly, provide a list of features that you will implement or algorithms that you will implement.  Break this list into two parts:
  * Short list of things you will implement for a grade  (i.e., you expect to get a good grade if you execute on all of these)
  * List of at most 1 or 2 “nice to haves” if you find yourself ahead of schedule

* __Expected visual deliverables.__ Example images/videos or other assets that you want your project to be able to create.  Often the best projects come when a student group has an image in mind that they want to create at the beginning, and then all work is focused on implementing the algorithms necessary to create that image.

* Optional: a list of dependencies that your project will be based on.  This might mean starter code you've already found on the internet (or from one of the CS248 assignments).  Or a technical paper/publication/blog post that you will use as a reference.  It might mean datasets or models that you've already found online.  We just want to clearly understand what you are starting with.

## Project Report and Video Submission

We require both a report and video hand-in, as described below. But you will receive a single overall grade for the project.  There are no predefined rubrics as all projects are slightly different -- but use the proposal or communication with the staff to establish expectations about grades. **One team only needs one submission (report + video)**

### Report Hand-in ###

The report should brief, but sufficient to convey everything you did.  In general this can be done in 2-3 pages. It's fine to go above this limit, especially if it's due to including good pictures of your results. Remember, the main point of the write up is to give the staff an overview of what the functionality you have implemented and its technical complexity.  Self-selected projects should take care to really explain what was done. 

Overall the final writeup hand-in should be a zip file submitted on Gradescope that includes the following components:

1. __Your writeup__, in pdf format, called `writeup.pdf' which includes:
 * Your name(s)
 * Project title.
 * A description of the functionality you have implemented. For example "I have implemented triangulate() function that takes a non-triangular mesh and divides it into triangles using the algorithm given in ..." Adding details about your implementation is welcomed, since it will help us grasp the complexity of the functions and the difficult of the work done.
 * Example assets you created (e.g.., a screenshot)

2. __Your assignment code.__  We do not anticipate trying to build or run your code.  We would like it only for potential review.

### Video Hand-in ###

Your demo video is a separate hand-in on __Canvas__ (not Gradescope). Your demo video should be 1920x1080 (1080p) if possible, and no longer than 90 seconds (shorter is fine), and encoded in standard video formats like .mp4 or H.264. The video should be limited to 90 seconds, and can include anything you wish.  Your video should provide evidence you implemented the set of features your writeup claims, as well include any demonstration of the best visuals your project has to offer.  As you can see in the examples from prior years, adding audio to you demo is encouraged for fun!
