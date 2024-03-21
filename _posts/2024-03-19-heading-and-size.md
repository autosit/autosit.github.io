---
layout: post
title: High precision extended object tracking
category: SF
---
## Background

As maritime surface autonomy is tackling more challenging use cases such as urban passenger ferries and unmanned cargo transport the need for precision increases. It is not sufficient to merely detect and track other vessels. 
The autonomy system must also know something about the size of other vessels in order to calculate feasible safety margins. 
Furthermore, autonomy system should be able to estimate the course and velocity of other vessels as accurately as possible, in order to plan its own trajectory. This is achieved by methods of extended object tracking (EOT). 

We have developed an EOT method based on Gaussian Processes that is suitable for marine vessels. This method models the perimeter a target vessel as a Gaussian Process, which is estimated from lidar data. 

However, in all closed-loop experiments so far we have used simpler tracking methods based on the point measurement assumption. The current state of the art in point-based tracking is the VIMMJIPDA tracker, which uses multiple motion models to improve the velocity estimation. 


|<img src="{{site.url}}/assets/headingests.png" width="700"> | 
| Example of lidar data where both the correct and a wrong heading estimate may seem plausible. |


## Scope


The primary goal of this project is to equip the Gaussian Process EOT method with multiple motion models, thereby improving its performance and building a bridge between the two approaches to vessel tracking. A secondary goal is to further improve the resulting method by fusion with camera data which also can provide information about the velocity and size of other vessels.


## Proposed Tasks
### Specialization project
1. Make yourself familiar with current theory and implementations of GP-EOT and VIMMJIPDA. 
2. Replace the current process model of the GP-EOT with a process model that utilizes both constant velocity models and a constant turn-rate model in parallel. 
3. Perform simulations, and investigate how multiple motion models affect the performance. 
4. Report your findings. 

|<img src="{{site.url}}/assets/lidarcam.png" width="700"> | 
| Example of lidar data superimposed on a camera image after calibration. |


### Master thesis

For the master thesis, the goal is to also include camera. This can be done in a variety of ways. One possibility is to build on a master thesis from the spring 2023, where the GP-EOT is being enhanced by optical flow measurements from camera. 
Another possibility is to focus on the information that can be extracted from YOLO bounding boxes and object masks. 
Yet another possibility is to directly estimate the vessel pose from the camera images. 

## Prerequisites
[TTK4250](https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet) is recommended background knowledge. 


## Supervisors
Main supervisor: [Edmund Brekke](http://www.ntnu.no/ansatte/edmund.brekke).<br>
Co-supervisor: [Martin Baerveldt](https://www.ntnu.no/ansatte/martin.baerveldt).<br>

## References
* M. Baerveldt, E. Lopez and E. Brekke (2023). "<a href="hhttps://ieeexplore.ieee.org/document/10224156">Extended target PMBM tracker with a Gaussian Process target model on LiDAR data.</a>" Proceedings of Fusion 2023.
* A. Hem (2021). "<a href="hhttps://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2781021?show=full&locale-attribute=no">Maritime multi-target tracking with radar and asynchronous transponder measurements.</a>" MSc thesis, NTNU. 

|<img src="{{site.url}}/assets/modelprobs.png" width="570"> | 
| Example of how multiple motion models can attain different probabilities depending on the behavior of a boat. |

