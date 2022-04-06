---
layout: post
title: AIS-guided radar clustering
category: SF
---
## Background

To ensure safe operation for autonomous vessels at sea, their ability to correctly perceive their surroundings is essential. To achieve a satisfactory situational awareness several sensors and communication systems are used. Vessels can be equipped with radars, lidars, and cameras, and in addition to onboard sensors the Automatic Identification System (AIS) transmits information about surrounding ships. By combining the use of different types of sensors, so called sensor fusion, one can benefit from the best properties of individual sensors. This is one of the goals of the [Autosit] project.
 
|<img src="{{site.url}}/assets/radar_illustration.pdf" width="700"> | 
| Different clustering schemes. From [Hem2021]|


This project concerns the use of AIS measurements to help a radar-utilizing tracking system. AIS measurements are received from the surrounding ships which are equipped with AIS transponders. These AIS measurements contain information regarding the ID of the ship, its position, velocity, size, and much more. However, not all ships transmit AIS measurements, and the measurements can arrive infrequently. This means that an autonomous ship must mainly rely on radar and other exteroceptive sensors. However, the AIS measurements contain valuable information which can help greatly with keeping track of surrounding ships.

When using radar in a target tracker, the individual radar detections of a single target must be grouped together and represented as a single point. While a large ship will result in several radar detections, the input to a target tracker will often only be a single coordinate. This is often done with an unsupervised clustering algorithm, a challenging problem due to the different characteristics of the detected objects. For example, the algorithm should be able to cluster all detections from a container ship while also being able to keep two kayaks in separate clusters. This is where the AIS measurements can be utilized. Any large ship will transmit its position, velocity, and size, well before it is within range of the radar. This information can then be used to create an adaptive clustering algorithm, hopefully mitigating the problem of low performance clustering methods. 

|<img src="{{site.url}}/assets/ClusterAnalysis_Mouse.svg" width="700"> | 
| Different clustering schemes. From: https://commons.wikimedia.org/w/index.php?curid=11765684|

## Scope
The project aims at developing a radar clustering method for maritime use, which utilizes information from incoming AIS measurements. 

## Proposed tasks for the 5th year project
The main goals of the specialization project will be to become familiar with the underlying mathematics, sensors and methods, and to implement a radar clustering algorithm which can receive input from AIS measurements. The proposed tasks are
*	Get to know the characteristics of radar and AIS measurements, and how these can be used in target tracking
*	Acquire knowledge of established radar clustering methods
*	Implement a radar clustering method which allows for target size input from AIS
*	Develop a method for predicting the size of ships detected by the radar, based on incoming AIS measurements
*	Test the method on real and simulated data, and compare the results with a method not using AIS input




## Proposed tasks for the master’s thesis
For the master’s thesis, the inclusion of the radar clustering process from the project can be included in a larger tracking framework, to be tested on experimental data. Another option is to combine the use of AIS in extended object tracking, which shares some similarities with the tasks from the project, but as part of a larger target tracking structure.

## Prerequisites
The candidate should have had the course [TTK4250 Sensor Fusion], or take it in parallel with the specialization project. Some experience in machine learning would be beneficial.



## References
Martin Ester, Hans-Peter Kriegel, Jörg Sander, and Xiaowei Xu. 1996. "[A density-based algorithm for discovering clusters in large spatial databases with noise.][Ester1996]" In Proceedings of the Second International Conference on Knowledge Discovery and Data Mining (KDD'96). AAAI Press, 226–231.

Audun Gullikstad Hem. "[Maritime multi-target tracking with radar and asynchronous transponder measurements.][Hem2021]" Master’s thesis, NTNU, September 2021 

J. A Sagild, A. G. Hem, and E. F. Brekke. "[Counting technique versus single-time test for track-to-track association.][Sagild2021]" In International Conference on Information Fusion, Sun City, 2021. 



## Contact

Supervisors: [Audun Hem], [Edmund Brekke].  

[Audun Hem]: www.ntnu.edu/employees/audun.g.hem
[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Ester1996]: https://www.aaai.org/Papers/KDD/1996/KDD96-037.pdf?source=post_page
[Hem2021]: https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2781021
[Sagild2021]: https://ieeexplore.ieee.org/document/9626911
[Autosit]: https://www.ntnu.edu/autosit
[Autosea]: https://www.ntnu.edu/autosea
[Milliampere]: https://www.ntnu.edu/autoferry
[TTK4250 Sensor Fusion]: https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet