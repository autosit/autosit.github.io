---
layout: post
title: Bridging distributions
category: LTP
---
## Background

A collision avoidance (COLAV) system for autonomous vessels depends on its future predictions of the motion of other vessels. 
This is typically done by means of a Kalman filter or extended Kalman filter. The simplest model suitable for moving vessels is the constant velocity (CV) model,
where deviations from straight motion are modeled by white process noise. To cover all the possibilities of future behavior with this model its plant noise strength has to be fairly large,
and this leads to very large uncertainties when the model is used over time horizons measured in minutes or beyond. 
An alternative to the CV model is the constant turn-rate (CT) model which typically is used to model maneuvers. While this model sometimes can yield more accurate predictions, we must have some idea about the turn-rate to use it. As yet another alternative, several MSc theses affiliated with the Autosea project have explored fundamentally data-driven methods for vessel prediction [Hexeberg2017] [Dalsnes2016]. 

The middle ground between model-driven and data-driven prediction methods remains largely unexplored.
As a fundamental research question, we ask whether knowledge about a ships possible destination harbors can be used to improve the prediction, without additional historical data. 
This line of reasoning has recently been pursued by researchers at University of Cambridge [Ahmad2016], where they introduced something called bridging distributions to model this kind of information. 

|<img src="{{site.url}}/assets/predictionproblem.png" width="670"> | 
| The fundamental problem of long-term prediction: Standard kinematic models yield very large uncertainties after a couple of minutes. One must guess the other vessel's intentions if more accurate predictions are desired. | 

## Scope

The goal of the specialization project will be to study the bridging density concept and its potential for long term vessel prediction. 
This approach can be tested on the same AIS data as were used in [Hexeberg2017] and [Dalsnes2016], or on data that will be recorded as part of the Autoferry project during the summer or early autumn 2019. It is also a goal to benchmark different prediction techniques against each other. 

## Proposed Tasks for the 5th year project

* Study and summarize different potential long-term prediction techniques, including conventional kinematic models, mean-reverting processes, bridging distributions, the modified neighbor course distribution method of [Dalsnes2016], etc. 
* Implement and evaluate the bridging distributions approach in simulated scenarios. 
* Implement and evaluate the bridging distributions approach on real data. 
* Benchmark it against one or more of the methods mentioned above.
* Write report. 

## Proposed Tasks for the master thesis

Several variations of MSc projects are possible, depending on the findings of the specialization project. Some suggestions are proposed below. 

* Experiment with introducing elements of machine learning. Can the stricter frames provided by bridging distributions framework make it easier to learn behaviors than in a pure data-driven approach?
* Utilization of class information. Should we expect Hurtigruta, a frigate and a fishing boat to approach different harbors? 
* Utilization of online AIS information and/or integration with a multi-target tracking system. 

This project can be expanded into a PhD or integrated PhD for a candidate with sufficient skills, background knowledge and motivation. 

|<img src="{{site.url}}/assets/ais-data-trd.png" width="670"> | 
| Historical AIS data show many patterns for how ships tend to move. Understanding of these patterns can be used to plan trajectories so that dangerous situations are prevented from arising.  | 

## References
* Ahmad et al. (2016). "<a href="https://ieeexplore.ieee.org/document/7765149">Bayesian Intent Prediction in Object Tracking Using Bridging Distributions.</a>" IEEE Transactions on Cybernetics , vol. 48, no. 1. [Ahmad2016]  
* Hexeberg, S. (2017). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2452108">AIS-based Vessel Trajectory Prediction for ASV Collision Avoidance.</a>" MSc thesis, NTNU. [Hexeberg2017]  
* Dalsnes, B. (2018). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2557943">Long-term Vessel Prediction Using AIS Data.</a>" MSc thesis, NTNU. [Dalsnes2018]

## Contact

Supervisors: [Edmund Brekke] and [Adil Rasheed].  

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Adil Rasheed]: https://www.ntnu.no/ansatte/adil