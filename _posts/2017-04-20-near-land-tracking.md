---
layout: post
title: Near-shore target tracking with map uncertainty
subtitle: 
category: SF
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. Target tracking is a key capability of autonomous vehicles moving in environments with traffic, as the autonomous vehicle needs to keep track of all other moving objects in its vicinity, and predict their future movement. Target tracking entails processing of data from various exteroceptive sensors, such as radar, lidar or camera. The radar in particular is an important sensor, but it suffers from extensive returns from land. Most of these returns are masked out, but map inaccuracies leads to some measurements near land. These measurements will cause false track estimates to appear near shore.

These false tracks may cause problems when a ship moves close to shore. The measurements from the real target may be associated with the track created from the land measurements, and the ship will not be discovered.

## Scope
In this project, the goal is to improve tracking of targets near land. There are two main approaches to this problem; either estimating the errors in the map online, or label the stationary tracks near land to allow moving tracks to form. Occupancy grids are an example of the first, while measures such as track coherence described in [this](http://ieeexplore.ieee.org/abstract/document/5603530/) paper may be of use in the latter.

## Proposed Tasks for the autumn project

1. Conduct a literature survey on various methods for map estimation, and tracking methods.
2. Suggest an approach for tracking targets near land. Test the method in simulations.
3. Test the method on real data, which will be provided by the Autosea project.
4. Write report.

## Proposed Tasks for the master thesis

The tasks for the master thesis will be finalized during the autumn project, but a few key points will be

- Compare several methods for tracking targets near land.
- Test the methods on a more challenging data set.
- Write thesis.

## Prerequisites
Required background knowledge:

- Experience in either Matlab, Python or C++.
- TTK4115 Linear System Theory.

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)
