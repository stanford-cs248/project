# Stanford CS248A Final Projects

## Due dates

1. The project proposal is due as soon as possible, earlier proposals will get quicker feedback.
2. Your final project demo video is due on __Monday, March 16th__ at 8 PM.
3. Your final project hand-in (writeup + code) is due on Tuesday __March 17th at 3:00pm__.
4. The project proposal deadline is "soft" in that we strongly encourage you to submit a proposal, but the proposal is not graded.  The purpose of the project proposal is to give you an opportunity to put your plans down on paper so you can get feedback from the staff about whether the project is too easy or too hard before it is too late. The writeup and video deadlines are hard deadlines --- __there are no late days__

__We will have a final project celebration and watch party to watch all the project videos as a group during our final exam slot on Tuesday March 17th from 3:30-5pm__. All on-campus students in the class is expected to come in person. We will give exemptions on a case-by-case basis.

## Summary

For the final assignment in this course you are free to design your own project. The only guidelines are as follows:

1. We love it when students get artistically creative with projects (we want to see some great final pictures and animations!), but a major portion of the assignment should be a technical component.  For example, creating a complex scene in 3D modeling package like [Blender](https://www.blender.org/) or implementing a mini-game in [Unity](https://unity.com/) via their level-editing tools is not a well-targeted final project for CS248A.  However, implementing a technique discussed in class in Unity would be a reasonable project.

2. Since the project spans only about two weeks our expectations are that you attempt a project that is a bit smaller than the work on the first three programming assignments, and then keep going if you meet your initial goals before the deadline.  In creating your proposal we want to you design a project that is challenging, but can reasonably be done by the deadline.  __Keep in mind you likely have other course projects and obligations during this time as well.__

3. Just like with all course programming assignments, you can work in teams of up to two students.

4. A good template for a project would be to dream up an image or video you want to create and then find an example of your vision in the form of an image/video. In your proposal show the image that you have in mind (e.g., download a photo, illustration, or someone else's computer-generated image from the internet as an example to convey your goals). Once you have an image in mind, then all your project work can just be focused on implementing the algorithms necessary to create an approximation to that image.

Please feel encouraged to discuss project ideas with your classmates and the staff on Ed or during office hours. To allow the staff to help you make sure your project is appropriately related to themes from the class and is appropriately scoped for the given amount of time, we ask you to submit a short project proposal. (see below for details).

## A Few Project Ideas ##

We will release example demo videos from a number of prior projects on Canvas/Panopto (the same place lecture videos are hosted).  You are encouraged to design your own project, but here are some examples to get you thinking:

* __Ray Tracing 3D Gaussians__: Implement a ray tracer of 3D Gaussians (stored in a BVH) would be a great final project. An even better final project would be to implement recovery of 3D Gaussians from images. You've already done it for meshes. A good reference is [here](https://gaussiantracer.github.io/). 

* __More Advanced Implicit Surface Rendering__:
You have a ray marcher of SDFs, you could add new primitives to your ray tracer and make a complex scene of SDFs. See (https://iquilezles.org/articles/raymarchingdf/) for many examples of how powerful this technique is. Just make sure you had some heft to this project beyond implementing a few functions from that web site. I'd like to see you envision a scene (e.g., find a photo online) and attempt to recreate parts of the scene with implicits.

* __Accurate camera simulation__: For for your path tracer has only simulated a pinhole camera, but what about real camera systems with lenses that focus on a particular part of the scene, or demonstrate motion blur for moving objects.  See [here](https://graphics.stanford.edu/papers/camera/) for camera simulation or [here](http://psgraphics.blogspot.com/2016/02/motion-blur-in-ray-tracer.html) for motion blur.

* __New primitive types or light types__: Add support to your ray tracer for new primitive types, like [subdivision surfaces](https://graphics.stanford.edu/~boulos/papers/subdiv_tr.pdf) or new light types, like an environment map.  How do you importance sample environment maps? (Hint: see [PBRT](https://pbr-book.org/))

* __Investigating More Spatial Acceleration Data Structures__:
 You've implemented BVH construction and traversal to speed up ray/scene intersection. Time to implement some more data structures! Implement two additional spatial acceleration data structures: we recommend an octree and a KD-tree. In production and game engine design, special care is taken when choosing which spatial acceleration data structure to use. Engineers have to consider the specific requirements of the scene and the advantages/disadvantages of each data structure. To that end, please research the advantages and disadvantages of each of your data structures (BVH + two more). Then, for each data structure, create one scene that showcases the data structure’s advantage, and one scene that showcases the data structure’s disadvantage. (You should have at least 6 scenes by the end.)

* __Volume Path Tracer__:
  Want to render clouds and smoke that are actually lit by light sources. These ``volumetric'' objects that can be pathtraced just like the cubes and spheres in the Cornell Box. Extend your path tracer to support volumetric path tracing. Here are some resources to get you started:
  https://cs.dartmouth.edu/~wjarosz/publications/novak18monte-sig.html
  https://cseweb.ucsd.edu/~tzli/cse272/wi2023/homework2.pdf
  Then show us some of your beautiful renders of volumetrics!

* __Spectral Path Tracer__:
  Extend your path tracer to support spectral rendering.  Each ray will be associated with one (randomly chosen) wavelength of light. Shooting many rays per pixel means that all wavelengths will be sampled inside a pixel, and you'll be able to render effects like the [seperation of light by a prism](https://blender.stackexchange.com/questions/1602/light-spectrum-dispersion-effect-in-blender) or a rainbow!

* __Neural Importance Sampling__:
  Can neural networks be used to help sample when ray tracing a scene? In class, we talked about different importance sampling techniques; in Neural Importance Sampling [Muller 19], authors describe a manner to fit neural networks to sample distributions in scenes. Check it out! http://jannovak.info/publications/NIS/index.html

* __Stylized Shaders, Pixel Art Shaders__:
  In programming assignment 3, you learned how to raytrace photorealistic images of 3D scenes. Now, imagine you can render a 3D scene in a non-photorealistic way, with a specific art style. Stylized shaders can manipulate light, color, texture, and edge detection to achieve a look that resonates with particular artistic movements or personal aesthetics. They offer a versatile toolset for artists and developers to craft visuals that are expressive, mood-setting, and distinct from the conventional realism in 3D graphics.
  There are many shader styles you can implement. One of the most popular ones is the Toon/Cel Shader. You can read more about it on [Wikipedia](https://en.wikipedia.org/wiki/Cel_shading).

* __Stylization of Meshes__:
  Similar to non-photorealistic pixel shaders, we can render geometry in non-photorealistic ways! Check out this fun paper: [Cubic Stylization by Hsueh-Ti Derek Liu and Alec Jacobson](https://www.dgp.toronto.edu/projects/cubic-stylization/). Imagine you have a squishy toy that you can mold into a shape that's kind of like a cube, but still looks like the toy. That's what this paper’s 3D styling trick does with digital shapes. The authors found out that you can make shapes look more like cubes if you treat their surfaces like stiff paper that only folds at sharp angles, not like cloth that can bend smoothly. By adjusting how the surfaces of the shape fold, we can keep the important details while giving it that cubey look. Try this for a fun geometry project!

* In the past, some students have done projects involving Apple's [AR-Kit](https://developer.apple.com/augmented-reality/).

* If you are interested in real-time 3D graphics engine programming, write a 3D renderer from scratch using a modern GPU-accelerated grapshics API like Direct 12 or Vulkan.

* A big idea these days is using machine learning to determine how to combine a small number of supersamples into a final high quality resolved result.  The result is that images produced with only a small number of samples per pixel look as it they were rendered with much higher sample counts. See techniques like [morphological anti-aliasing](http://www.iryoku.com/mlaa/), which predated use of modern deep learning techniques, or more modern techniques based on DNNs for image-to-image transfer (called in DLSS by NVIDIA).

You can also choose to do one of the prior programming assignments from this class. Although these assignments do not involve GPU programming in Slang.

* __Draw SVG__: A 2D SVG renderer. See the starter code [here](https://github.com/stanford-cs248/draw-svg).

* __Mesh editor:__ Make a simple editor for polygon meshe. See the start code [here](https://github.com/stanford-cs248/Cardinal3D?tab=readme-ov-file).

* __Shaders__: You are given a simple real-time renderer and a simple 3D scene. However, the starter code implements only very simple material and lighting models, so rendered images do not look particularly great.  You will improve the quality of the rendering by implementing a number of lighting and material shading effects using the GLSL, OpenGL's [shading language](https://thebookofshaders.com/01/), as well as some OpenGL client code in C++. Through this project option the point is to get basic experience with modern shader programming, and to build understanding of how material pattern logic, material BRDFs, and lighting computations are combined in a shader to compute surface reflectance. There are countless ways you can keep going by adding more complex materials and lighting.
  Starter Code: <https://github.com/stanford-cs248/shading>

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
