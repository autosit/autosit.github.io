---
layout: post
title: Uncertainty management in scenario-based model predictive control for collision avoidance
category: COLAV
---
## Background
Collision avoidance (COLAV) methods typically attempt to deviate sufficiently from the desired path to ensure that no collision will occur. The decision about how much to deviate must be made in the presense of several different kinds of uncertainties. Even if other ships move along straight lines, imperfect sensors are needed to estimate their velocities, and these estimates may suffer from significant uncertainties. Such uncertainties are typically quantified using probability theory, e.g., by means of covariance matrices. 

Most collision avoidance methods do not facilitate any probabilistic treatment of such uncertaintites. However, in the recently developed simulation-based model predictive control (SB-MPC) approach to collision avoidance, it is possible to include this kind of information in the cost function. 

![Different types of uncertainty]({{site.url}}/assets/uncertainties.png)

## Scope
The goal of this project is to develop and test a version of the SB-MPC method that deals with kinematic estimation uncertainty, primarily uncertainty pertaining to velocity estimates. The method should be extensively tested in a variety of scenarios to indicate whether accounting for uncertainties leads to more reliable collision avoidance.  

## Proposed Tasks for the 5th year project

1. Define scenarios, make simulation engine and implement SB-MPC method. This can to a large extent be based on previous work in the Autosea project.
2. Make kinematic data of target ships (positions and velocities) corrupted by noise similar to what one would get in a real sensor fusion system. 
3. Test the SB-MPC method without accounting for these noises. 
4. Modify the SB-MPC method to account for these noises, and test the resulting method.
5. Write report. 

## Proposed Tasks for the master thesis

The project work aims to be extended into a master thesis for the spring of 2018.  For the master thesis, we are interested in more general investigations of risk assessment for collision avoidance methods. While it can be argued that most COLAV methods implicitly attempt to minimize the risk of collision, an explicit treatment of collision risk, or more precisely collision probabilities, is not part of most, if any, collision avoidance methods. 

In this project the goal is to investigate whether it is possible to predict the probability of a collision, with basis in uncertainty inputs such as those investigated in the specialization project. 

Tasks for the master’s project:

1. Discuss collision risk quantification approaches in the literature.
2. Implement one or more collision probability measures in simulation.
3. Use Monte-Carlo simulations to analyze the validity of the calculated probability.
4. If time permits, elaborate the risk measure with additional sensor fusion uncertainties etc.
5. Write report.


## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)
