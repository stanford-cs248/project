# CS248 Final Projects

This repository is located at https://github.com/stanford-cs248/project. 

## Due dates

1. The project proposal is due __Fri March 1st__ 11:59:59 PM.  Please submit via Canvas. 
2. The 60-second video presentation of your project is due __Wed March 20__ 6:00 PM. This video can be anything you wish, but it should be designed to show off the best visuals your project has to offer.
3. The find project writeup is due __Thu March 21st__ at 11:59:59 PM.

## Summary

For the final assignment in this course you are free to design your own project. The only guidelines are as follows:

1. We love it when students get artistically creative with projects (we want to see some great final pictures and animations!), but a major portion of the assignment should be a technical component.  For example, creating a complex scene in Blender or implementing a mini-game in Unity via their level-editing tools is not a well-targeted final project for CS248.  However, implementing a technique discussed in class in Unity, would be a reasonable project.

2. Since the project spans approximately three weeks of class, our expectations are that you attempt a project that is approximately the scope of 2.5 course programming assignments.  In crating your proposal we want to you design a project that is challenging, but can reasonably be done in three weeks.  (Keep in mind you likely have other courses projects and finals during this time as well.)

3. Just like with all course programming assignments, you can work in teams of up to two students.

Please feel encouraged to discuss project ideas with your classmates and the staff on Piazza or during office hours. To allow the staff to help you make sure your project is appropriately related to themes from the class and is appropriately scoped for the given amount of time, we ask you to submit a short project proposal, which is worth 5% of your Final Project grade. (see below for details).

## A Few Project Ideas ##

You are of course encouraged to design your own project, but here are some examples to get you thinking: 

* Extend the SVG renderer from Assignment 1 so it can render as many SVG files from the web as possible.  This would involve adding support for new primitive types: spline curves, elipses, rotated images, fonts, text. Etc.  We recommend that you start by downloading some interesting SVG's and then continue to add features to your SVG renderer until it correctly renders them.

* Implement all of the extra credits for Assigment 2 (if you haven't done so already) such as mesh beveling, mesh decimation, etc. and use the resulting modeling tool to create a really cool mesh.  A good way to design the project is to first pick a mesh you want to create, and then add features to your tool to make it.

* Complete the Animation part of Assignment 2. (It is described on the Assignment 4 wiki.)  This involves a sampling of inverse kinematics, mass-spring systems, and keyframe animation.  

* Extend Assignment 3 to render more advanced shadows and materials.  For example, you could take a look at techniques like cascased shadow maps, screen-space ambient obscurance, environment mapping (by generating a cube map), or other, more advanced types of light sources, like linear-transformed cosines or spherical harmonic lighting.  Then design the coolest scene you can that shows off all the new features.  Or you could also start from a clean code base and write your own openGL (or WebGL renderer) for a scene.  For example, Prof. Kayvon is very interested in someone making a WebGL-based port of assignment 3.

## The Project Proposal ##

The proposal is due __Fri March 1st at 11:59:59 PM__ on Canvas. **You cannot use late days for the proposal!**

We expect a project proposal that is at most two pages long. (This is not a hard limit... expecially if you want to include images, but you get the point).  Please include the following sections in your proposal:

The proposal will have the following sections:

* Project Title:  A great title is catchy, but also descriptive!

* Names and SuNET ID's of the people working on the project

* A brief 1-to-2 sentence summary of your project plus a potential image or link to a video that shows off an example of something you'd like  For example: _"We are going to extend assignment 1 with support for drawing spline curves so that we can render SVGs with curves and arbitrary True-Type fonts. We want to be able to render an image that looks like XXXXX"_.  or "We are going to extend assignment 2 with support for mesh downsampling via the quadratic error metric.  We will use this implementation to generate meshes of various levels of detail that we will import into Unity and show how we can choose the right mesh to render as a character gets closer and farther from the camera on screen." 

* No more than a few paragraphs of description of what you will do.  Most importantly, provide a list of features that you will implement or algorithms that you implement.

* Example images/videos or other assets that you want your project to be able to create.  Often the best projects have an image in mind that they want to create, and then all work is focused on implementing the algorithms necessary to create that image.

* Optional: a list of dependencies that your project will be based on.  This might mean starter code you've already found on the internet (or from one of the CS248 assignments).  A technical paper/publication/blog post that you will use as a reference.  It might mean datasets or models that you've already found online.  We just want to clearly understand what you are starting with.  

## Video Presentation ##

The video presentation of your project is due Wed March 20 at 5:00pm on Canvas.  **You cannot use late days for the video presentation since we will immediately coalesce all videos together into a long video for the class to see on the 21st** 

## PRoject Report Submission 

The final project report is due Thu March 21st, 11:59:59 PM.  **You cannot use late days for the final project!** Full details of expectations for the report will be posted in the coming weeks.
