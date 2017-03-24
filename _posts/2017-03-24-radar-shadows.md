---
layout: post
title: Multi-target tracking in radar shadows
category: SF
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. TTarget tracking is an important capability of autonomous vehicles moving in environments with traffic, as the autonomous vehicle needs to keep track of all other moving objects in its vicinity, and predict their future movement. Target tracking entails processing of data from various exteroceptive sensors, such as radar, lidar or camera. 

Challenging situations occur when different targets are shadowing each other. In such scenarios, the radar tracker may be tempted to terminate the track on the shadowed target prematurely, something which could be dangerous in a collision avoidance system. 

## Scope
The key idea behind this project is that the probability that a target exists should be influenced knowledge about such shadows, through adjustment of its assumed probability of detection, which is a tuning parameter in the tracking method. This work will be based on the Integrated Probabilistic Data Association (IPDA) and multi-target extensions of this tracking method. 

## Proposed Tasks for the 5th year project

1. Conduct a literature study on tracking methods that use the concept of target existence. 
2. Implement a single-target IPDA that utilizes variable detection probability due to known static obstacles. 
3. Extend the scenario to moving objects casting shadows with known extents.
4. Compare with the results with standard methods (Ordinary IPDA, PDAF with M-out-of-N logic for track termination, MHT, etc.)
5. Write report.

## Proposed Tasks for the master thesis

In the master’s project the goal shall be to extend the developments of the 5th year project into a bona-fide multi-target tracking method for extended targets. 

## Prerequisites
Required background knowledge:

- Experience in either Matlab, Python or C++.
- TTK4115 Linear System Theory.

Useful, but not required, background knowledge:

- Courses in statistics, algorithms development and/or artificial intelligence.
- Experience with radar systems or machine vision.

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)
