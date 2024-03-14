---
layout: post
title: The spinning radar
category: SF
---
## Background

Radar plays a crucial role for maritime navigation, for three reasons: It can see further than other sensors. It is more resilient to bad weather conditions than other sensors. It provides both range and bearing measurements. The fact that it can measure distance, makes radar data much easier to work with than camera data, which do not provide any direct measurements of distance. The range-and-bearing measurements can typically be converted to Cartesian coordinates, so that linear measurement models can be used. 

 
|<img src="{{site.url}}/assets/radar_illustration.pdf" width="700"> | 
| Different clustering schemes. From [Hem2021]|

However, traditional maritime radars tend to use a rotating beam, whose period can be a few seconds. This artefact is often ignored in literature on maritime radar tracking and localization. As an example, in the pipeline described in [Wilthil, Flåten And Brekke (2017)][WFB] radar measurements were translated from polar coordinates to Cartesian coordinates at the time they were observed, but the entire radar scan was subsequently processed with the final time of the radar scan as a common time stamp, leading to a potential time error up to 2.7 seconds. 

In target tracking it is possible to use the correct times, and this was solved in  [Hem (2022)][Hem2022]. 
For radar-based navigation, such as techniques for simultaneous localization and mapping (SLAM) or radar-based odometry, an additional challenge arises because the radar pose is unknown and something that we want to estimate. Still, it is possible to compensate for the motion distortion by assuming a constant velocity during each radar scan [(Burnett 2021)][Buernett2021]. 




|<img src="{{site.url}}/assets/ClusterAnalysis_Mouse.svg" width="700"> | 
| Different clustering schemes. From: https://commons.wikimedia.org/w/index.php?curid=11765684|

## Scope
The main goal of this project is to include radar rotation compensation into methods for radar-based localization for autonomous surface vessels. 


## Proposed tasks for the 5th year project
The main goals of the specialization project will be to become familiar with the underlying mathematics, sensors and methods, and to implement a radar clustering algorithm which can receive input from AIS measurements. The proposed tasks are
*	xx
*	xx
*	xx
*	xx
*	xx




## Proposed tasks for the master’s thesis
For the master’s thesis, the inclusion of the radar clustering process from the project can be included in a larger tracking framework, to be tested on experimental data. Another option is to combine the use of AIS in extended object tracking, which shares some similarities with the tasks from the project, but as part of a larger target tracking structure.

## Prerequisites
The candidate should have had the course [TTK4250 Sensor Fusion], or take it in parallel with the specialization project. 



## References
Martin Ester, Hans-Peter Kriegel, Jörg Sander, and Xiaowei Xu. 1996. "[A density-based algorithm for discovering clusters in large spatial databases with noise.][Ester1996]" In Proceedings of the Second International Conference on Knowledge Discovery and Data Mining (KDD'96). AAAI Press, 226–231.

Audun Gullikstad Hem. "[Maritime multi-target tracking with radar and asynchronous transponder measurements.][Hem2021]" Master’s thesis, NTNU, September 2021 

J. A Sagild, A. G. Hem, and E. F. Brekke. "[Counting technique versus single-time test for track-to-track association.][Sagild2021]" In International Conference on Information Fusion, Sun City, 2021. 



## Contact

Supervisors: [Edmund Brekke].  

[Audun Hem]: www.ntnu.edu/employees/audun.g.hem
[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[WFB]: https://link.springer.com/chapter/10.1007/978-3-319-55372-6_13
[Hem2022]: https://ieeexplore.ieee.org/document/9931947
[Buernett2021]: https://ieeexplore.ieee.org/document/9327473
[Sagild2021]: https://ieeexplore.ieee.org/document/9626911
[Autosit]: https://www.ntnu.edu/autosit
[Autosea]: https://www.ntnu.edu/autosea
[Milliampere]: https://www.ntnu.edu/autoferry
[TTK4250 Sensor Fusion]: https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet