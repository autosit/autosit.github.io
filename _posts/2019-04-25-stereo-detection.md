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

Bla bla 

## Proposed Tasks for the 5th year project

* Bla bla
* Write report. 

## Proposed Tasks for the master thesis

Several variations of MSc projects are possible, depending on the findings of the specialization project. Some suggestions are proposed below. 

* Bla bla
* Bla bla 
* Bla bla 

## References
* Tangstad, E. (2017). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2452113">Visual Detection of Maritime Vessels.</a>" MSc thesis, NTNU.
* Grini, S. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/grini_simen_msc_reduced.pdf">Object Detection in Maritime Environments: Systematic Training and Testing of Deep Learning-based Detection Methods for Vessels in Camera Images.</a>" MSc thesis, NTNU. 
* Kamsvåg, V. (2018). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/kamsvaag_msc.pdf">Fusion between camera and lidar for autonomous surface vehicles.</a>" MSc thesis, NTNU.

## Contact

Supervisors: [Edmund Brekke] and [Annette Stahl]


[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Annette Stahl]: www.ntnu.edu/employees/annette.stahl