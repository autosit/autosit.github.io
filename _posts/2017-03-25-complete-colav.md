---
layout: post
title: A complete collision avoidance system
category: MISC
---
## Background
Collision avoidance for autonomous vehicles entails a processing pipeline that involves the following tasks:
1. Detection of other vehicles in sensor data
2. Tracking and prediction of other vehicles
3. Decision as to whether other vehicles are likely to collide with ownship.
4. Determination of suitable collision avoidance maneuver if needed.
5. Guidance and control according to collision avoidance maneuver.
 

## Scope
The goal of this project is to develop a simulator that involves all five steps of the pipeline.

## Proposed Tasks
a. Implement a line-of-sight-based vessel motion simulator.
b. Implement a simple simulator of data from a maritime radar mounted on a moving vessel.
c. Implement a tracking method based on the Probabilistic Data Association Filter (PDAF) or multiple hypothesis tracking (MHT).
d. Implement a collision avoidance (COLAV) method, such as the Velocity Obstacle (VO), or a method based on Model Predictive Control (MPC).
e. Implement an interface between the tracking method and the COLAV method. 
f. Write report. 

Solutions to many of these tasks will be available from previous research in the Autosea projects. The candidate must stitch together different solutions, or develop new solutions when this is more convenient.

The project work aims to be extended into a master thesis for the spring of 2018. Tasks for the master thesis include:

- Identify strengths and weakness of the system developed in the 5th year project, and suggest and implement solutions to some of the weaknesses.
- Include treatment of land in the simulator, both in the sensor and in the collision avoidance. 
- Write report.

## Prerequisites
Required background knowledge:

- TTK4115 Linear System Theory.
- TTK 4190 Guidance and Control of Vehicles.
- Strong programming skills in Matlab, Python or C++.


## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Supervisors 
Main supervisor: [Edmund Brekke](http://www.ntnu.no/ansatte/edmund.brekke).

