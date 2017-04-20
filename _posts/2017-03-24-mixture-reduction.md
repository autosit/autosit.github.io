---
layout: post
title: Track-before-detect
subtitle: Tracking of nearly invisible targets
category: SF
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. Target tracking is a key capability of autonomous vehicles moving in environments with traffic, as the autonomous vehicle needs to keep track of all other moving objects in its vicinity, and predict their future movement. Target tracking entails processing of data from various exteroceptive sensors, such as radar, lidar or camera. The tracking problem consists of two sub-tasks: Filtering and data association. The former task is about estimating the state vectors of the targets. The latter task is about identifying which measurement (e.g., radar reflection) comes from which target, so that the correct measurements are used in the filtering. 

    There are, roughly speaking, two kinds of solutions to data association: Searching for the best hypothesis, or averaging over all feasible hypotheses. The former approach leads to Multiple Hypothesis Tracking ([MHT](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=1102177)) while the latter approach leads to Joint Probabilistic Data Association ([JPDA](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1145560)). 

## Scope
In this project, the goal is to combine these two approaches in order to make more robust and efficient tracking methods, combining the strenghts of MHT and JPDA. Ultimately, this is an exercise in [mixture reduction](http://www.diva-portal.org/smash/get/diva2:858322/FULLTEXT02.pdf): We want to reduce the number of components in our description of the posterior distribution of the target state in accordance with some information-theoretic cost function. We will start in the single-target scenario, and gradually expand the complexity by introduction two or more targets as well as existence uncertainty. 

![Example of mixture reduction in PDAF]({{site.url}}/assets/diverprediction2.png)

## Proposed Tasks for the 5th year project

1. Conduct a literature survey on various approaches to mixture reduction in the target tracking literature.
2. Conduct a literature study on relevant techniques from probablistic machine learning, including variational Bayes techniques.
3. Implement one or two mixture reduction techniques based on variational Bayes inference for single-target tracking.
4. Compare with the results from single-target versions of JPDA and MHT.
5. Write report.

## Proposed Tasks for the master thesis

1. Extend the results from the 5th year project by studying the simplest possible multi-target situation: When two targets are close enough to each other to be confused with each other.
2. Depending on interests and results so far, the next step should either be to extend the work by including existence uncertainty, or by including multiple maneuver models. 
3. Test the methods on simulations as well as real data.
4. Write report.


## Prerequisites
Required background knowledge:

- Experience in either Matlab, Python or C++.
- TTK4115 Linear System Theory.

Useful, but not required, background knowledge:

- TDT4120 Algorithms and Data Structures (Additional courses in algorithm construction or artificial intelligence may be useful as well).
- Knowledge of Markov random fields (for example from TMA4250 - Spatial Statistics.)
- Experience with radar systems or machine vision.

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)
