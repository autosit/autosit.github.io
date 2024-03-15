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
While a simple method for rotation compensation has been investigated in automotive autonomy, no such analysis has been done for maritime radar-based localization. The specialization project should therefore try to answer the questions: How much does it matter? Can it be improved? To make this analysis easier, a simulation-based approach is recommended. 

The proposed tasks are
*	Simulate data that mimic real data for radar-based vessel odometry and SLAM with a rotating radar.
*	Implement radar rotation compensation assuming constant velocity during each radar scan. 
*	Analyze impact of rotation compensation for a variety of maneuvering scenarios. 
*	Implement and experiment with motion models that relax the piecewise straight motion assumption. 
*	Write the report. 


## Proposed tasks for the master’s thesis
For the master’s thesis, the ambition is to move from simulated data to the real world. Relevant radar data are available from a variety of projects. It may also be desirable to collect new radar data with a high-resolution radar that we plan to purchase. This could also be part of a paid summer internship in the summer 2024. 

## Prerequisites
The candidate should have had the course [TTK4250 Sensor Fusion], or take it in parallel with the specialization project. Background in computer vision or radar signal processing may also be useful. 



## References

Keenan Burnett, Angela Schoellig and Timothy Barfoot. 2021. "[Do We Need to Compensate for Motion Distortion and Doppler Effects in Spinning Radar Navigation?][Buernett2021]". In IEEE Robotics and Automation Letters. Vol. 6, No. 2,  p. 771-778.

A. G. Hem, and E. F. Brekke. "[Compensating radar rotation in target tracking.][Hem2022]" In International Conference on Information Fusion, Sun City, 2021. 

Wilthil, Flåten & Brekke (2017): "[A target tracking system for ASV collision avoidance based on the PDAF][WFB]", in Sensing and Control for Autonomous Vehicles, Springer. 



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