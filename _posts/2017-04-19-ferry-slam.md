---
layout: post
title: Simultaneous localization and mapping for autonomous ferry
category: SF
---
## Background
Autonomous vehicles need to determine where they are relative to their surroundings, and they may also need to construct a map of their surroundings based on data from imaging sensors. This chicken-and-egg-problem is known as simultaneous localization and mapping (SLAM). Fully fledged SLAM is often redundant, as information about vehicle position and surroundings can be obtained from GNSS and map databases, respectively. Nevertheless, the capability of SLAM may be nice to have in case of GNSS breakdown etc. 

## Scope
The topic of this project is SLAM for an autonomous ferry that is planned to operate between Ravnkloa and Brattøra. Currently, preliminary experiments are being conducted with DNV-GL’s ReVolt as a prototype, and a Velodyne lidar sensor will be available for experiments in the autumn. The work will involve recording data from the inertial navigation system and the Velodyne lidar mounted on ReVolt, and processing these data off-line by means of off-the-shelf SLAM methods. 

## Proposed Tasks for the 5th year project

1. Conduct a literature survey on SLAM methods suitable for lidar in harbor environment.
2. Make yourself familiar with ROS and Hector-SLAM. 
3. Record lidar and navigation data.
4. Implement Hector-SLAM on the recorded data.
5. Analyze results and write report.

## Proposed Tasks for the master thesis

The project work aims to be extended into a master thesis for the spring of 2018. Depending on the interest of the students, several important challenges may be addressed:

- Experimenting with other SLAM appraoches than Hector-SLAM.
- Introduce pose-graph optimization in Hector-SLAM.
- Integration of map information in the SLAM framework.
- Online experiments with the SLAM software installed on surface vehicle.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)

## References

* Kohlbrecher et al. (2011): “[A Flexible and Scalable SLAM System with Full 3D Motion Estimation](http://ieeexplore.ieee.org/document/6106777/)”, in Proceedings of 2011 IEEE International Symposium on Safety, Security, and Rescue Robotics.
* Durrant-Whyte, H. & Bailey, T. (2006): “[Simultaneous localization and mapping: Part I](http://ieeexplore.ieee.org/document/1638022/)”, IEEE Robotics & Automation Magazine, vol. 13, pp. 99-108.