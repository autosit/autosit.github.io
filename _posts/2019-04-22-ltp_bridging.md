---
layout: post
title: Bridging densities
category: LTP
---
## Background

A collision avoidance (COLAV) system for autonomous vessels depends on its future predictions of the motion of other vessels. 
This is typically done by means of a Kalman filter or extended Kalman filter. The simplest model suitable for moving vessels is the constant velocity (CV) model,
where deviations from straight motion are modeled by white process noise. To cover all the possibilities of future behavior with this model its plant noise strength has to be fairly large,
and this leads to very large uncertainties when the model is used over time horizons measured in minutes or beyond. 
An alternative to the CV model is the constant turn-rate (CT) model which typically is used to model maneuvers. While this model sometimes can yield more accurate predictions, we must have some idea about the turn-rate to use it. As yet another alternative, several MSc theses affiliated with the Autosea project have explored fundamentally data-driven methods for vessel prediction [Hexeberg2017] [Dalsnes2016]. 

The goal of this project is to explore the middle ground between model-driven and data-driven prediction methods. 
As a fundamental research question, we ask whether knowledge about a ships possible destination harbors can be used to improve the prediction, without additional historical data. 
This line of reasoning has recently been pursued by researchers at University of Cambridge [Ahmad2016], where they introduced something called bridging densities to model this kind of information. 


## Scope

The goal of the specialization project will be to study the bridging density concept and its potential for long term vessel prediction. 
This approach can be tested on the same AIS data as were used in 

## Proposed Tasks for the 5th year project

bla bla

* bla bla
* bla bla
* bla bla
* bla bla
* bla bla

## Proposed Tasks for the master thesis

bla bla


## References
[Ahmad et al. (2016). "Bayesian Intent Prediction in Object Tracking Using Bridging Distributions." IEEE Transactions on Cybernetics , vol. 48, no. 1.][Ahmad2016]  
[Hexeberg, S. (2017). "AIS-based Vessel Trajectory Prediction for ASV Collision Avoidance." MSc thesis, NTNU.][Hexeberg2017]  
[Dalsnes, B. (2018). "Long-term Vessel Prediction Using AIS Data." MSc thesis, NTNU.][Dalsnes2018]

## Contact

Supervisor: [Edmund Brekke].  

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
