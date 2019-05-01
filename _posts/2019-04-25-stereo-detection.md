---
layout: post
title: Improved ship detection through stereo vision
category: EOT
---
## Background

Situational awareness for an autonomous vehicle (e.g., autonomous ship) depends on sensors that can perceive obstacles and other vehicles, 
and track and predict their motion so that collisions are avoided. The first step in this processing pipeline is to detect other vehicles in the raw sensor images. 
For radar and lidar this can be done by fairly straightforward thresholding and clustering operations. For optical or infrared camera images this is significantly more complex.

Classical detection methods have used a wide variety of techniques based on background subtraction, edge detection and spatial-temporal filtering. 
Such methods have in later years been outperformed by convolutional neural networks (CNNs), which currently dominate the state of the art. Several recent MSc thesis associated with Autosea project have explored CNN-based ship detection (Tangstad2017, Grini2019). While the results are very promising, it is still not clear that the detection performance is good enough to rely on these methods in an autonomous collision avoidance system. 

In particular, the following challenges are important (Kamsvåg 2018):
* Buildings are often mistaken for being ships. 
* The CNNs may struggle to detect ships when they cover too few pixels to recognize details and overall shape. 
* The CNNs may struggle to discern nearby and overlapping ships. 

A possible solution is to include range information in the detection process. This can be achieved by fusion with active sensors (e.g., lidar), 
by structural light or by providing a baseline, either by lifting the camera up or by combining two or more cameras in stereo vision. 
This project will explore the last of these options. 





## Scope

The primary goal of this project is to explore how much stereo vision can improve visual vessel detection.
This will involve recording relevant data and developing new detection methods. Based on the results, the candidate may during the MSc thesis choose to go more in-depth into stereo vision,
or explore alternative approaches for utilizing range information. 

The candidate will install a stereo camera system on a suitable vessel such as the autonomous ferry Milliampere or the manned/unmanned sport vessel Telemetron. 

## Proposed Tasks for the 5th year project

The following tasks are proposed for the specialization project:

* Conduct a litterature survey on visual detection and relevant research results in stereo vision. 
* Install a stereo camera system on a suitable vessel such as the autonomous ferry Milliampere or the manned/unmanned sport vessel Telemetron. 
* The camera system must be synchronized with the GPS-based navigation system, and possibly also with other sensors such as radar, lidar and 360 degree camera systems. 
* Record a sufficient amount of data to be used for training and testing of detectors. 
* Implement a detection method. This may be something like a CNN that takes two images simultaneously. However, classical techniques or combinations of classical techniques and CNNs should also be considered. 
* Analyze the performance of the detection method, and compare with the results from the networks that were trained by Grini (2019). 
* Write report. 



## References
* Tangstad, E. (2017). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2452113">Visual Detection of Maritime Vessels.</a>" MSc thesis, NTNU.
* Grini, S. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/grini_simen_msc_reduced.pdf">Object Detection in Maritime Environments: Systematic Training and Testing of Deep Learning-based Detection Methods for Vessels in Camera Images.</a>" MSc thesis, NTNU. 
* Kamsvåg, V. (2018). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/kamsvaag_msc.pdf">Fusion between camera and lidar for autonomous surface vehicles.</a>" MSc thesis, NTNU.
* Liszewski, A. (2019). "<a href="https://gizmodo.com/elon-musk-was-right-cheap-cameras-could-replace-lidar-1834266742">Elon Musk Was Right: Cheap Cameras Could Replace Lidar on Self-Driving Cars, Researchers Find.</a>" Gizmodo magazine.

## Contact

Supervisors: [Edmund Brekke] and [Annette Stahl]


[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Annette Stahl]: www.ntnu.edu/employees/annette.stahl