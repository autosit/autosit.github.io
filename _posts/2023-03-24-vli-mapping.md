---
layout: post
title: Creating a game-world from camera and lidar data
category: NA
---
## Background
Researchers at NTNU are currently developing an autonomous ferry designed for carrying pedestrians and cyclists between Ravnkloa and Brattøra. The development of a robust collision avoidance system for this ferry can benefit from a proper 3D model akin to a "game scene" of the area. Such a 3D model can potentially aid in the localization of the ferry itself, the detection of other boats, and in simulating scenarios.

![Brattøra]({{site.url}}/assets/brattora.jpg)

## Scope
The goal of this project is to see if we can develop such a "game scene" from our sensor data, specifically using optical camera and lidar data. The proposed scope of this project is to use open-source SLAM and structure from motion libraries to solve this. Several smaller or larger problems will probably be detected through the specialization project which can be a part of the master thesis topic.

## Proposed Tasks
### Specialization project
1. Use [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM) or [LOAM](http://wiki.ros.org/loam_velodyne) on data from the Trondheim canal.
2. Generate a point cloud and create a mesh ([code ex1](https://pointclouds.org/documentation/tutorials/greedy_projection.html), [code ex2](https://github.com/hhoppe/Mesh-processing-library))
3. Put textures on the mesh by projecting it onto the camera images.
4. Compare this to using a structure from motion library (only cameras).
5. Evaluate:
   1. Which is better?
   2. Can we quantify the uncertainty?
   3. Which improvements are needed for localization, detection, or simulation?

### Master thesis
For the master thesis, two main branches can be followed. Either improve the model or use the model. The specialization project might show that improvements are necessary in order to use the model at all, in which case this must be addressed first. Otherwise one could address one or more of the tasks of localization, detection, and scenario simulation.

|![Simulation]({{site.url}}/assets/simunity.png)|
|A still frame from a simulator of the regionx|

## Prerequisites
The candidate should have some prior knowledge of computer vision or SLAM, and for the master thesis good knowledge about optimization might be needed. Otherwise, courses on these topics should be taken in parallel. Relevant courses are [TTK4255](https://www.ntnu.no/studier/emner/TTK4255#tab=omEmnet), [TTK21](https://www.itk.ntnu.no/emner/fordypning/TTK21), and possibly [TTK4250](https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet).


## Supervisors
Main supervisor: [Edmund Brekke](http://www.ntnu.no/ansatte/edmund.brekke).<br>
Co-supervisor: [Lars-Christian Ness Tokle](https://www.ntnu.no/ansatte/lars-christian.n.tokle).<br>

![UrbanFerge]({{site.url}}/assets/Ferge.png)
