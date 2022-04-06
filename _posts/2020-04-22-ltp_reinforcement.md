---
layout: post
title: COLREG-compliant path following and collision avoidance with moving obstacles in the Trondheim fjord
category: nonsense
---
## Background

A collision avoidance (COLAV) system for autonomous vessels depends on its future predictions of the motion of other vessels. 
This is typically done by means of a Kalman filter or extended Kalman filter. However, for long-term prediction such techniques are of limited value. Instead, the autonomous system must attempt to guess the future intentions of other vessels. 
Machine learning can be used to extract knowledge about typical ship behaviours from large amounts of data from the Automatic Identification System (AIS) that have been stored. Furthermore, reinforcement learning (RL) can also be used by the autonomous ship, or its digital twin, to learn rational own behaviours. 



## Scope

This project concerns the problem of anticipating the intentions of another ship on time intervals in the order of minutes. Over such time intervals, one can typically expect the ship to perform certain manoeuvres (e.g., go straight, approach its destination port, make a complete evasive manoeuvre), but all such predictions will be highly uncertain. The goal of this project is to develop methods that are able to combine relevant sources of information to make predictions over such time intervals. 

## Proposed Tasks for the 5th year project

The project will build upon the work by Meyer et al and will be realized through the following potential tasks

* Data collection and preprocessing: This will involve collecting data from different sources as well as generating data (CAD models, weather data) if required and then pre-processing them for further analysis.
* Extending our reinforcement learning framework incorporating multiagent simulation capabilities
* More extensive incorporation of AIS data in the reinforcement learning framework
* Extension of the collision avoidance regulations in the current framework
* Devising better RL training strategies
* Run an ensemble of simulations using the trained agents to quantify uncertainty associated with long-term vessel predictions

## Proposed Tasks for the master thesis

The specialization project is intended to be continued as a master thesis project. 


## References
* Meyer E., Robinson, H., Rasheed, A., and San, O., (2020). "<a href="https://doi.org/10.1109/ACCESS.2020.2976586">Taming an autonomous surface vehicle for path following and collision avoidance using deep reinforcement learning.</a>" IEEE Access.
* Meyer E., Heibergh A., Rasheed A. and San O.,  "COREG-compliant path following and collision avoidance with moving obstacles in the Trondheim fjord using Deep Reinforcement Learning". In preparation.

## Contact

Supervisors: [Adil Rasheed], [Edmund Brekke] and [Morten Breivik]

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Adil Rasheed]: https://www.ntnu.no/ansatte/adil
[Morten Breivik]: https://www.ntnu.edu/employees/morten.breivik