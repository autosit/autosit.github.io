---
layout: post
title: Collision probabilities
category: LTP
---
## Background
Risk evaluations are an obvious component of a collision avoidance (COLAV) system. But what exactly is meant by risk? Is it a qualitative or a quantitative concept? A related concept is probability. Whether or not a collision is likely to happen if a ship follows a given course is clearly something that matters for whether that course is safe. 
It is hoped that automatic COLAV methods that are able to calculate and make use of such probabilities and risk measures can make better decisions than more basic COLAV methods, and also assist human captains through decision support systems. 

There are several tricky issues that must be addressed when attempting to define and calculate such probabilities. 
The steering of a ship is not just a random process, but something that is governed by willful actions. 
Interactions between different ships play a central role. 
If we ignore these concerns, it will seem natural to model the motion of the ships as stochastic processes in two dimensions, for example governed by the constant-velocity with white-noise acceleration model. 
It is then of interest to evaluate the probability that two such processes at some point in the future (presumably not too far into the future) come sufficiently close to each other. 

## Scope
The main goal of the project is to provide formulas or algorithms for reliable quantification of collision probability
under sufficiently general circumstances to be of practical utility. The work will build on a master thesis being written this semester. 

## Proposed Tasks for the 5th year project

The focus in the 5th year project shall be on establishing a conceptual framework, rather than on computational feasibility. 

1. Write a survey on collision risk approaches in the scientific literature. 
2. Formulate the collision probability problem mathematically under reasonably general assumptions.
3. Identify simplified cases and propose solutions for the collision probabilities in these cases. 
4. Verify that the evaluated probabilities make sense, ideally both from an intuitive perspective and according to simulations (i.e., a frequentist perspective).
5. Write report.

## Proposed Tasks for the master thesis

The project work aims to be extended into a master thesis for the spring of 2020. Depending on the interest of the students, several directions are possible:

- Combination with approaches to long-term prediction, as explored in the bridging densities project or in the master theses of Hexeberg (2017) and Dalsnes (2018). 
- Further generalization of the work done in the specialization project. 
- Approximations needed to utilize the work in COLAV methods.
- Design of new MPC-based COLAV methods capable of using collision probabilities or related risk measures in a meaningful way. 

## Prerequisites

This project is suitable for a candidate with high degree of mathematical maturity. The candidate should have a good understanding of topics such as Monte-Carlo integration, stochastic processes, series expansions and partial differential equations. 

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)

## References

* Tengesdal, T., Johansen, T. A. and Brekke, E. (2022): [“Ship Collision Avoidance Utilizing the Cross-Entropy Method for Collision Risk Assessment”](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828), IEEE Transactions on Intelligent Transportation Systems.