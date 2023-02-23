# Stanford CS248A Final Projects

## Due dates

1. The project proposal is due __Friday March 3rd__ 11:59:59 PM, but feel __strongly encouraged__ to submit earlier to get quicker feedback.
2. Your final project demo video is due on Monday __March 20th__ at 5 PM.
3. Your final project handin (writeup + code) is due on Tuesday __March 21st__ at 3:30pm.

The project proposal deadline is "soft" in that we strongly encourage you to submit a proposal, but the proposal is not graded.  The purpose of the project proposal is to give you an opportunity to put your plans down on paper so you can get feedback from the staff about whether the project is too easy or too hard before it is too late. The writeup and video deadlines are hard deadlines --- __there are no late days__

__We will have a final project celebration and watch party to watch all the project videos as a group during our final exam slot on Tuesday March 21th from 3:30-5pm__. Everyone in the class is highly encouraged to come in person, but we will give the option to attend the watch party online for those that want to.

## Summary

For the final assignment in this course you are free to design your own project. The only guidelines are as follows:

1. We love it when students get artistically creative with projects (we want to see some great final pictures and animations!), but a major portion of the assignment should be a technical component.  For example, creating a complex scene in 3D modeling package like [Blender](https://www.blender.org/) or implementing a mini-game in [Unity](https://unity.com/) via their level-editing tools is not a well-targeted final project for CS248A.  However, implementing a technique discussed in class in Unity would be a reasonable project.

2. Since the project spans approximately three weeks of the quarter (and that period of time includes an exam), our expectations are that you attempt a project that is approximately the scope of course programming assignment (perhaps a little bit more work if you have the time).  In creating your proposal we want to you design a project that is challenging, but can reasonably be done in three weeks.  __We encourage you to be ambitious, but keep in mind you likely have other course projects and obligations during this time as well.__

3. Just like with all course programming assignments, you can work in teams of up to two students.

4. Usually the best projects start with dreaming up an image or video you want to create and finding an example of that image/video. In your proposal show an image that you have in mind (e.g., download a photo, illustration, or someone else's computer-generated image) from the internet as an example to convey your goals. Once you have an image in mind, then all your project work can just be focused on implementing the algorithms necessary to create that image.

Please feel encouraged to discuss project ideas with your classmates and the staff on Ed or during office hours. To allow the staff to help you make sure your project is appropriately related to themes from the class and is appropriately scoped for the given amount of time, we ask you to submit a short project proposal. (see below for details).

## A Few Project Ideas ##

We have released example demo videos from a number of prior projects on Canvas/Panopto (the same place lecture videos are hosted).  We encourage you to take a look at what students have tried in the past.  However, you'll notice that some of these prior projects involved animation algorithms.  Animation was previously covered in CS248A, but has now been moved to CS248B.  I'd prefer that your projects focus on topics closer to what we learn about in CS248A, but if you are really, really interested in doing an animation project (the one documented on the Cardinal3D wiki), come talk to me.

You are encouraged to design your own project, but here are some examples to get you thinking:

* Extend the SVG renderer from Assignment 1 so it can render as many SVG files from the web as possible.  This would involve adding support for new primitive types: spline curves, elipses, rotated images, fonts, text. etc that you might not have had a chance to implement during Assignment 1.  We recommend that you start by downloading some interesting SVG's and then continue to add features to your SVG renderer until it correctly renders them. (You might have to improve the starter code's SVG parser to support these more advanced effects as well.)

* If you are interested in real-time rendering, extend the Shader assignment (one of the Assignment 3's) to render more advanced shadows and materials.  For example, you could take a look at techniques like "Cascaded shadow maps", "screen-space ambient obscurance", environment mapping (by generating a cube map), or other, more advanced types of light sources, like [linearly-transformed cosines](https://eheitzresearch.wordpress.com/415-2/) or spherical harmonic lighting.  Then design the coolest scene you can that shows off all the new features.

* Extend the path tracer assignment with new features. This might include:
   * [Accurate camera simulation](https://graphics.stanford.edu/papers/camera/) or [motion blur](http://psgraphics.blogspot.com/2016/02/motion-blur-in-ray-tracer.html)
   * Support for ray tracing new primitive types, like [subdivision surfaces](https://graphics.stanford.edu/~boulos/papers/subdiv_tr.pdf).
   * Extend your renderer to do multi-spectral rendering, where you trace different rays for different wavelengths, allowing you to render prism-like effects [like this] (https://blender.stackexchange.com/questions/1602/light-spectrum-dispersion-effect-in-blender).
   * Add important-sampled environment maps to your ray tracer.
   * If you are feeling ambitious (advanced mode warning!!!) try more advanced importance sampling techniques like [practical path guiding](https://studios.disneyresearch.com/wp-content/uploads/2019/03/Practical-Path-Guiding-for-Efficient-Light-Transport-Simulation.pdf) or [neural path importance samping](https://dl.acm.org/doi/abs/10.1145/3341156?casa_token=3ItxOk6eb6QAAAAA:ANc4xVSwPbtbvZ8AVCh8S2KUfhV_-KtSmtrw_4Enx1iHTZxefhauDK6iYQBBhGNjhFkVUv8Qr6zr).  Some students might be very interested in all the importance sampling work targeting real-time ray tracing, such as NVIDIA's [ReSTIR](https://research.nvidia.com/publication/2020-07_spatiotemporal-reservoir-resampling-real-time-ray-tracing-dynamic-direct) algorithm for significantly reducing the number of samples needed to get good results in a many light situation or consider the [2022 version](https://research.nvidia.com/publication/2022-07_generalized-resampled-importance-sampling-foundations-restir) or [ReSTIR-GI](https://research.nvidia.com/publication/2021-06_restir-gi-path-resampling-real-time-path-tracing).

* Some students get really interested in procedural modeling, where you create expressions that create complex geometric scenes from a small number of simple rules.  Google topics like "procedural modeling", "L-systems", the site <a href="https://www.shadertoy.com/">shadertoy.com</a> is inspirational. (See <a href="https://cineshader.com/gallery">CineShader.com</a> for top shadertoy examples.)

* Another procedural-modeling project, would be to take recent algorithms for generating floorplans, furniture layouts, etc and build a system for generating random 3D scenes.  If you are interested in doing this come talk to Kayvon since it would be useful for one of his research projects.  Inspiration might come from projects like [ProcTHOR](https://procthor.allenai.org/). I'd love to have a well-written piece of C++ code that generates scenes like those.

* __If you are interested in performance__, take your Assignment 1 or Assignment 3 Path tracer any parallelize it onto multiple cores and even using SIMD instructions. (We recommend using [ISPC](https://ispc.github.io/) for generating SIMD code for a CPU. Ray tracing is aready parallelized across cores, but it would be interesting to consider SIMD ray tracing and multi-core parallel BVH construction.

* In the past, some students have done projects involving Apple's [AR-Kit](https://developer.apple.com/augmented-reality/).

* If you are interested in real-time 3D graphics engine programming, write a 3D renderer from scratch using a modern GPU-accelerated grapshics API like Direct 12 or Vulkan.

* A big idea these days is using machine learning to determine how to combine a small number of supersamples into a final high quality resolved result.  The result is that images produced with only a small number of samples per pixel look as it they were rendered with much higher sample counts. See techniques like [morphological anti-aliasing](http://www.iryoku.com/mlaa/), which predated use of modern deep learning techniques, or more modern techniques based on DNNs for image-to-image transfer.

* Implement corners and creases in Catmull-Clark subdivision.  (This on its own is a little small for a project, it might be part of a project that also includes additional extra credits from Assignment 2.)

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

We require both a report and video handin, as described below. But you will receive a single overall grade for the project.  There are no predefined rubrics as all projects are slightly different -- but use the proposal or communication with the staff to establish expectations about grades. **One team only needs one submission (report + video)**

### Report Handin ###

The report should brief, but sufficient to convey everything you did.  In general this can be done in 2-3 pages. It's fine to go above this limit, especially if it's due to including good pictures of your results. Remember, the main point of the write up is to give the staff an overview of what the functionality you have implemented and its technical complexity.  Self-selected projects should take care to really explain what was done. 

Overall the final writeup handin should be a zip file submitted on Gradescope that includes the following components:

1. __Your writeup__, in pdf format, called `writeup.pdf' which includes:
 * Your name(s)
 * Project title.
 * A description of the functionality you have implemented. For example "I have implemented triangulate() function that takes a non-triangular mesh and divides it into triangles using the algorithm given in ..." Adding details about your implementation is welcomed, since it will help us grasp the complexity of the functions and the difficult of the work done.
 * Example assets you created (e.g.., a screenshot)

2. __Your assignment code.__  We do not anticipate trying to build or run your code.  We would like it only for potential review.

### Video Handin ###

Your demo video is a separate handin on __Canvas__ (not Gradescope). Your demo video should be 1920x1080 (1080p) if possible, and no longer than 90 seconds (shorter is fine), and encoded in standard video formats like .mp4 or H.264. The video should be limited to 90 seconds, and can include anything you wish.  Your video should provide evidence you implemented the set of features your writeup claims, as well include any demonstration of the best visuals your project has to offer.  As you can see in the examples from prior years, adding audio to you demo is encouraged for fun!
