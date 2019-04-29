---
layout: post
title: Detection and pose estimation by means of synthetic camera data
category: EOT
---
## Background

Situational awareness for an autonomous vehicle (e.g., autonomous ship) depends on sensors that can perceive obstacles and other vehicles, 
and track and predict their motion so that collisions are avoided. The first step in this processing pipeline is to detect other vehicles in the raw sensor images. 
For cameras this is typically done by means of convolutional neural networks (CNNs). Several recent MSc thesis associated with Autosea project have explored CNN-based ship detection (Tangstad2017, Grini2019). 

Since CNNs use machine learning, it is important to have enough training data. The data should support extrapolation to all relevant scenes that one may encounter. 
To support this, training procedures for CNNs typically expand the training set by adding mirrored and rotated versions of the images, etc. 
Nevertheless, one is bound by the amount of images that one has recorded in the real world. 

One possible approach to significantly increase the number of training images is to simulate additional images. While such images alone would be an unreliable training set, 
they can be used together with real images using transfer learning. This allows experimentation with adjustments of pose angle, distance from camera, impact of occlusions, light conditions, etc. Simulation of camera data is generally nontrivial, and is typically done with game engines or similar 3-d graphics software such as Unreal, Unity or Open GL. 

A human observer may not only be able to recognize the presence of a ship in an image, but also additional information about the ship such as its attitude. 
This is of obvious importance in a COLAV system
For machine learning algorithms to achieve the same capability, the methods must be trained on data containing sufficient variability of the variables of interest. 


## Scope

The goal of this specialization / master project is to explore the utility of simulated camera in the context of ship detection by means of machine learning methods. 
The focus will be on theory and programming. Several data sets that can serve as inspiration and also be used for validation purposes are available already, as are CNNs trained on these data sets. Some experimental work may be required towards the end of the master project to obtain data suitable for verification of attitude estimation. 


## Proposed Tasks for the 5th year project

The 5th year project will focus on automatic simulation of camera data in a maritime environment. It is also a goal to explore whether augmenting real data with simulated data can improve training of CNNs for visual vessel detection. 

The following tasks are proposed for the specialization project:

1. Make an informed choice between the different simulation tools available. 
2. Obtain or construct CAD models of the most important elements in the surroundings. 
3. Simulate camera data with ships at different ranges, attitudes, occlusion conditions etc. 
4. Train pre-trained neural networks (YOLO, SSD, Faster-RCNN) on the simulated images using transfer learning. 
5. Investigate how this affects the performance of the neural networks on real data. 
6. Write report. 

This specialization project can be done in collaboration with another specialization project on [Simulation of sensor data for Milliampere], but each student has to write a separate report.

## Proposed Tasks for the MSc thesis

In the MSc thesis the main goal will be to investigate the role played by attitude in the simulation-based detection. The main challenge is to identify how existing machine learning methods can be adapted to the joint detection and pose recognition problem. References such as (Sans-Muntadas 2019) may serve as inspiration. 


## References
* Tangstad, E. (2017). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2452113">Visual Detection of Maritime Vessels.</a>" MSc thesis, NTNU.
* Kamsvåg, V. (2018). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/kamsvaag_msc.pdf">Fusion between camera and lidar for autonomous surface vehicles.</a>" MSc thesis, NTNU.
* Grini, S. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/grini_simen_msc_reduced.pdf">Object Detection in Maritime Environments: Systematic Training and Testing of Deep Learning-based Detection Methods for Vessels in Camera Images.</a>" MSc thesis, NTNU. 
* Sans-Muntadas, A. et al. (2019). "<a href="https://reader.elsevier.com/reader/sd/pii/S2468601818300191?token=00F31C37E53FDBDA590029A2114E54FF84EC6C9076728369CB319FE96DB516A41446CB0DBA59563177F22BDB59147FA1">Learning an AUV docking maneuver with a convolutional neural network.</a>" IFAC Journal of Systems and Control.


## Contact

Supervisors: [Edmund Brekke], [Annette Stahl] and [Rudolf Mester]


[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Annette Stahl]: www.ntnu.edu/employees/annette.stahl 
[Rudolf Mester]: www.ntnu.edu/employees/rudolf.mester
[Simulation of sensor data for Milliampere]: https://autoferry.github.io/sf/2019/04/25/simcam/