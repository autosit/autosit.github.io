---
layout: post
title: Multi-sensor extended object tracking
category: SF
---
## Background

Situational awareness (SITAW) for an autonomous vehicle (e.g., autonomous ship) depends on sensors that can perceive obstacles and other vehicles, 
and track and predict their motion so that collisions are avoided. 
Popular sensors include maritime radar, lidar, optical cameras and infrared cameras. 

Traditional maritime SITAW systems have been centred around the maritime radar, which is the only reliable sensor when the sensing system must cover several kilometers on the open sea. However, on shorter ranges lidars and cameras can provide richer information, which can be of crucial importance when margins of errors are smaller due to increased congestion or more confined environments (e.g., in harbours). In particular, both in lidar data and in camera data it is possible to make inference about the shape and extent of other boats. 

While the traditional tracking methods from the 70s and 80s have assumed that all targets are points, more recent methods for extended object tracking (EOT) attempt to estimate the shapes of the targets. This is an active research area, which has not yet arrived at the same maturity as traditional tracking methods.  





## Scope

Bla bla


## Proposed Tasks for the 5th year project

The 5th year project will focus on Bla bla

The following tasks are proposed for the specialization project:

1. Make an informed choice between the different simulation tools available. 
2. Obtain or construct CAD models of the most important elements in the surroundings. 
3. Simulate camera data with ships at different ranges, attitudes, occlusion conditions etc. 
4. Train pre-trained neural networks (YOLO, SSD, Faster-RCNN) on the simulated images using transfer learning. 
5. Investigate how this affects the performance of the neural networks on real data. 
6. Write report. 



## Proposed Tasks for the MSc thesis

In the MSc thesis the main goal will be to investigate the role played by attitude in the simulation-based detection. Tasks include:

* Identify how existing machine learning methods can be adapted to the joint detection and pose recognition problem. References such as (Sans-Muntadas 2019) may serve as inspiration. 
* Train a machine learning method to recognize attitude
* Obtain a test data set. It is important that the test set is recorded such that a ground truth is available for pose, meaning that synchronization with other sensors and/or GPS/compass must be sufficiently accurate. 
* Test the joint detection and attitude recognition method, and quantify performance. 
* Write report. 

## Prerequisites

Background in machine learning, for example from TDT4171 Artificial intelligence methods or TDT4265 Computer vision and deep learning, will be useful. The candidate should take 
TTK21 VSLAM and TTK25 Computer Vision for Control in parallel with the 5th year project. 

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