# Stanford CS248 Final Projects

## Due dates

1. The project proposal is due __Thu Feb 27__ 11:59:59 PM.  Please submit via Canvas. 
2. The final project writeup is due at __Wed March 18th__ at 11:59 PM.
3. The 90-second video presentation of your project is due __Thu March 19__ 3:00 PM. This video can be anything you wish, but it should be designed to show off the best visuals your project has to offer.

The project proposal deadline is "soft" in that we'd like you to submit a proposal by this time, but the proposal is not graded.  It is only designed to give you an opportunity for feedback from the staff before it is too late. The writeup and video deadlines are hard deadlines --- there are no late days.

## Summary

For the final assignment in this course you are free to design your own project. The only guidelines are as follows:

1. We love it when students get artistically creative with projects (we want to see some great final pictures and animations!), but a major portion of the assignment should be a technical component.  For example, creating a complex scene in 3D model package like [Blender](https://www.blender.org/) or implementing a mini-game in [Unity](https://unity.com/) via their level-editing tools is not a well-targeted final project for CS248.  However, implementing a technique discussed in class in Unity, would be a reasonable project.

2. Since the project spans approximately three weeks of class, our expectations are that you attempt a project that is approximately the scope of 1.5 course programming assignments.  In creating your proposal we want to you design a project that is challenging, but can reasonably be done in three weeks.  (Keep in mind you likely have other courses projects and finals during this time as well.)

3. Just like with all course programming assignments, you can work in teams of up to two students.

Please feel encouraged to discuss project ideas with your classmates and the staff on Piazza or during office hours. To allow the staff to help you make sure your project is appropriately related to themes from the class and is appropriately scoped for the given amount of time, we ask you to submit a short project proposal. (see below for details).

## A Few Project Ideas ##

You are of course encouraged to design your own project, but here are some examples to get you thinking: 

* Extend the SVG renderer from Assignment 1 so it can render as many SVG files from the web as possible.  This would involve adding support for new primitive types: spline curves, elipses, rotated images, fonts, text. Etc.  We recommend that you start by downloading some interesting SVG's and then continue to add features to your SVG renderer until it correctly renders them.

* Implement all of the extra credits for Assigment 2 (if you haven't done so already) such as mesh beveling, mesh decimation, etc. and use the resulting modeling tool to create a really cool mesh.  A good way to design the project is to first pick a mesh you want to create, and then add features to your tool to make it.  In general, we consider this an "easier" project.

* Complete the Animation part of Assignment 2. (It is described on the Assignment 2 wiki.)  This involves a sampling of inverse kinematics, mass-spring systems, and keyframe animation.  

* If you haven't done so already, extend Assignment 3 to render more advanced shadows and materials.  For example, you could take a look at techniques like cascased shadow maps, screen-space ambient obscurance, environment mapping (by generating a cube map), or other, more advanced types of light sources, like [linearly-transformed cosines](https://eheitzresearch.wordpress.com/415-2/) or spherical harmonic lighting.  Then design the coolest scene you can that shows off all the new features.  Or you could also start from a clean code base and write your own openGL (or WebGL renderer) for a scene.  For example, Prof. Kayvon is very interested in someone making a WebGL-based port of assignment 3.

* Some students get really interested in procedural modeling, where you create expressions that create complex geometric scenes from a small number of simple rules.

* Implement a ray tracer from scratch that implements hard and soft shadows, reflections, and refractions.  A really nice implementation would also include path tracing (which is a major topic of CS348B, but you'd have to learn it on your own.)  A reference like [PBRT](https://www.pbrt.org/) would be very helpful.  This project should also include building a BVH acceleration structure for your ray tracer.

* In class we talked about closest point to X queries, but we only talked in detail about accelerating ray-scene intersection queries. An advanced project would attempt to write the fastest implementation you can of the following algorithm: given a point P, find the closest point (P2) to P in the scene.  (note this is a trickier problem them ray-scene intersection, since it's like finding the closest intersection involving any ray with origin P).  Please talk to Kayvon about this before attempting it as a good solution has implications to a research project.

* Last year some students did projects involving Apple's [AR-Kit](https://developer.apple.com/augmented-reality/).

* If you are interested in real-time 3D graphics engine programming, write a renderer from scratch using a modern GPU-accelerated grapshics API like Direct 12 or Vulkan.

* A big idea these days is learning how to combine a small number of supersamples into a final per-pixel resolved result.  The result is that images produced with only a small number of samples per pixel look as it they were rendered with much higher sample counts. See techniques like [morphological anti-aliasing](http://www.iryoku.com/mlaa/) which predate use of modern deep learning techniques, but more modern versions.

* Implement corners and creases in Catmull-Clark subdivision.  (this might be part of a project)


## The Project Proposal ##

Please submit a proposal via Canvas, ideally by 11:59pm on Thursday 2/27.  Your proposal can be short (2 pages max), but it should clearly state your plans for the project.  Please follow the guidlines/template below:

The proposal will have the following sections:

* __Project Title:__  A great title is catchy, but also descriptive!

* __Names and SuNET ID's__ of the people working on the project

* __Summary:__ A brief 2-3 sentence summary of your project goals plus a potential image or link to a video that shows off an example of something you'd like to create. For example: _"We are going to extend assignment 1 with support for drawing spline curves so that we can render SVGs with curves and arbitrary True-Type fonts. We want to be able to render an image that looks like..."._  or _"We are going to extend assignment 2 with support for mesh downsampling via the quadratic error metric.  We will use this implementation to generate meshes of various levels of detail that we will import into Unity and show how we can choose the right mesh to render as a character gets closer and farther from the camera on screen."_ 

* __Task list:__ No more than a few paragraphs of description of what you will do.  Most importantly, provide a list of features that you will implement or algorithms that you will implement.  Break this list into two parts:
  * Short list of things you will implement for a grade  (i.e., you expect to get a good grade if you execute on all of these)
  * List of at most 1 or 2 “nice to haves” if you find yourself ahead of schedule

* __Expected visual deliverables.__ Example images/videos or other assets that you want your project to be able to create.  Often the best projects come when a student group has an image in mind that they want to create at the beginning, and then all work is focused on implementing the algorithms necessary to create that image.

* Optional: a list of dependencies that your project will be based on.  This might mean starter code you've already found on the internet (or from one of the CS248 assignments).  Or a technical paper/publication/blog post that you will use as a reference.  It might mean datasets or models that you've already found online.  We just want to clearly understand what you are starting with.  

## Video Presentation ##

## Project Video and Report Submission 

The final project report and demonstration video is due Thur March 19st, at 11:59 PM.  **You cannot use late days for the final project!** 

The report should brief, but sufficient to convey everything you did.  In general this can be done in 2-3 pages. It's fine to go above this limit, especially if its due to including good pictures of our results. Remember, the main point of the write up is to give the staff an overview of what the functionality you have implemented and its technical complexity.   

Overall the components of a handin, which can be a zip file, include:

1. A pdf, called WRITEUP.PDF which includes:
  --Your name(s)
  --Project title. 
  --A description of the functionality you have implemented. For example "I have implemented triangulate() function that takes a non-triangular mesh and divides it into triangles using the algorithm given in ..." Adding details about your implementation is welcomed, since it will help us grasp the complexity of the functions and the difficult of the work done. 
  -- Example assets you created (e.g.., a screenshot)

2. Your assignment code.  We do not anticipate trying to build or run your code.  We would like it only for potential review.

3. Your demo video. This video should be 1920x1080 (1080p) if possible, no longer than 90 seconds (shorter is fine), and encoded in .mp4 or H.264. The video should be limited to 90 seconds, and can be anything you wish.  However, recommend you use the video to show off all the features you implemented. 
