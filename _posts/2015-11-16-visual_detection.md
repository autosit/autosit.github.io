---
layout: post
title: Visual detection and tracking
subtitle: Optical sensors for maritime collision avoidance
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. In addition to ship instrumentation such as RADAR and AIS, a human navigator relies on his vision as an important tool to avoid collisions at sea. The International Regulations for Avoiding Collisions at Sea (COLREGS) explicitly states that navigators should use their vision in addition to RADAR. As computer vision continues to show success in many robotics domains, including extraplanetary exploration on NASAs Curiosity Mars rover and many autonomous driving applications, it is likely that optical sensors can have a prominent role in autonomous collision avoidance at sea. 

## Scope
Obstacle avoidance is a requirement for autonomous ship operations. Therefore, other objects in the planned path of the ship need to be identified and tracked. Object detection with an optical sensor (camera) is one way to detect objects. However, this is challenging in maritime environments since objects at sea can be hard to distinguish from the waterline or hidden in waves. Furthermore, cameras have a limited range and objects far from the camera might be impossible to detect or cluttered by noise or other objects. In this project detection of marine vessels are the main priority. The algorithms developed in this project are not required to run in real-time, the focus is on detection performance and evaluation.

![Infrared image taken from an UAV]({{site.url}}/assets/infrared.jpg)

This project will look into object detection in camera images with two different approaches. The first approach is to investigate if objects at sea can be detected by a camera placed onboard the ship. The second will look into the use of an unmanned aerial vehicle (UAV) as an airborne sensor to detect objects. Both of these approaches have advantages and one important part of the project is to compare these. Both regular and infrared camera can be used in this project, but infrared images might be easier to work with because of the temperature difference between other vessels and the water. Some data is already available and an experiment with both a ship and UAV may be conducted during the fall.

## Proposed Tasks

1. Perform a litterature review over camera detection theory, algorithms and techniques in a maritime context.
2. Evaluate detection algorithms and propose a suitable solution for maritime object detection.
3. Implement a detection algorithm using e.g. OpenCV/Matlab/Python.
4. Test the detectors ability to track objects using standard tracking methods (i.e. Kalman Filter)
5. Present the results and discuss limitations and challenges.

## Prerequisites
This is a list of *recommended* prerequisites for this master project.

- Experience in either Matlab, Python or C++.
- Basic knowledge of computer vision or image processing. [TDT4265](http://www.ntnu.edu/studies/courses/TDT4265) is great, but not required.

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)
