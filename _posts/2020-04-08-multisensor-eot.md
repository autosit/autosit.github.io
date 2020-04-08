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

While the traditional tracking methods from the 70s and 80s have assumed that all targets are points, more recent methods for extended object tracking (EOT) attempt to estimate the shapes of the targets. This is an active research area, which has not yet arrived at the same maturity as traditional tracking methods.  Key challenges include the following:

* Different parametrizations of of extent are possible. These include random matrices, ellipses or more general star-convex shapes, Gaussian processes, etc. All come with different strengths and weaknesses, and are in general nontrivial to work with. 
* A multi-target EOT method should ideally consider all plausible partitions of the data into different combinations of extended objects. This leads to a data association problem that is much more complex than for traditional multi-target tracking. 
* Measurement models rely on approximations that are questionable and poorly understood (e.g., random matrices of Gaussian processes for lidar) or it may not even be clear how a measurement model should be formulated (for EOT based on cameras). 
* It is difficult to make a good process model that accounts for the subtle correlations between orientation and velocity. 

Nevertheless, the time may be ripe for a breakthrough in maritime extended object tracking. Reasons for optimism and ambition include the following:

* Significant progress on EOT have been made by handful of research groups, in particular at Chalmers University in Sweden. This includes a general framework for integration of EOT in the Poisson Multi-Bernoulli Mixture (PMBM) framework, which is the de facto gold standard for multi-target tracking. 
* The related problem of simultaneous localization and mapping (SLAM) has been extensively researched over the next decade. It may be possible to adapt techniques from SLAM to EOT (e.g., pose graph optimization).
 
## Scope

The goal of this combined specialization and MSc project is to develop an EOT algorithm that combines data from an active sensor (lidar) with data from a passive sensor (infrared or optical camera). 


## Proposed Tasks for the 5th year project

The following tasks are proposed for the specialization project:

* Data consolidation. Do interesting data exist? Make experiments or use the Experts-in-teams MilliAmpere digital twin. 
* Synchronization and calibration. 
* Literature review: Investigate relevant techniques, including different EOT algorithms, alternative pose estimation techniques (ICP, PCA) and structure-from-motion approaches. 
* Problem formulation: Identify missing building blocks in the above “lego collection”, and suggest possible fusion architectures. 
* Implement a scheme for multi-sensor joint tracking and pose estimation.  

## Proposed Tasks for the MSc thesis

In the MSc thesis the goal will be to integrate the work from the specialization project into the framework of multi-target tracking. 

* Conduct a literature survey on the most popular and relevant approaches to multi-target tracking. 
* Define a suitable state representation and motion model based on the findings from the specialization project. 
* Formulate measurement models for the sensors involved, so that Bayesian state estimation can be used. 
* Implement a Bayesian filter for the single-target multi-sensor EOT problem. 
* Include models for clutter, misdetections and multi-target association uncertainty. 
* Implement a multi-target multi-sensor EOT method. 

## Prerequisites

Useful courses include TTK4250 Sensor fusion, TTK21 VSLAM, TTK25 Computer Vision for Control  and TTK4255 Robotic Vision. The candidate should have taken some of these already, and considering taking the remaining courses in parallell with the specialization project. 

## References
* Granström, K., Baum, M. and Reuter, S. (2017). "<a href="http://isif.org/journal/12/2/1557-6418">Extended Object Tracking: Introduction, Overview and Applications.</a>" MSc thesis, NTNU.
* Kamsvåg, V. (2018). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/kamsvaag_msc.pdf">Fusion between camera and lidar for autonomous surface vehicles.</a>" MSc thesis, NTNU.
* Lopez, E. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/lopez_eot.pdf">LIDAR Extended Object Tracking of a Maritime Vessel using Gaussian Processes.</a>" Specialization project, NTNU. 
* Lauvsnes, M. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/lauvsnes_pose_estimation.pdf">Detection and pose estimation by
means of synthetic camera data.</a>" Specialization project, NTNU.


## Contact

Supervisors: [Edmund Brekke], [Annette Stahl] and [Rudolf Mester]


[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Annette Stahl]: www.ntnu.edu/employees/annette.stahl 
[Rudolf Mester]: www.ntnu.edu/employees/rudolf.mester
[Simulation of sensor data for Milliampere]: https://autoferry.github.io/sf/2019/04/25/simcam/