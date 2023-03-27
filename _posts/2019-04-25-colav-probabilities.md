---
layout: post
title: Collision probabilities
category: OTHER
---
## Background
Risk evaluations are an obvious component of a collision avoidance (COLAV) system. But what exactly is meant by risk? Is it a qualitative or a quantitative concept? We often think of risk as related to probability. This leads to the research question: Can we estimate the probability that a future collision will occur given some knowledge about the autonomous ship and other ships in its vicinity? 

In [(Tengesdal et al. 2020)] such probabilities were evaluated based on the assumption that the future trajectory of the obstacle ship can be modeled by a straight line motion. Then, the probability density function of the relative motion can be integrated over those initial states that would lead to a collision, to give the collision probability.  See also Example 5.4 on Page 80 in [the sensor fusion book] for a more elaborate explanation. The probabilities were used as input in the scenario-based model-prediction control (SB-MPC) COLAV method of [(Johansen et al. 2016)].

A slightly different approach was taken in [(Tengesdal et al. 2022)]. Here, an instantaneous collision probability was evaluated by integrating the target ship probability density function over the ownship safety zone. The Cross-Entropy method was used to implement a more efficient Importance sampler. However, the instantaneous interpretation is problematic if one wants to accumulate the probability of collision over several segments in a trajectory, because the sample time will affect the result. 

|<img src="{{site.url}}/assets/colavprobs.png" width="750" > | 
| <span style="color:#959595">Illustrations of the philosophies used in  [(Tengesdal et al. 2020)] and [(Tengesdal et al. 2022)]. </span> | 

## Scope
The main goal of the project is to develop a method for evaluating collision probabilities that is more efficient than [(Tengesdal et al. 2020)], but which retains the invariance to time step length. 

## Proposed Tasks for the 5th year project

The focus in the 5th year project shall be on exploring the collision probability problem. The following tasks and research questions should be addressed.

1. Write a survey on collision risk approaches in the scientific literature. Discuss assumptions, approximations, strengths and weaknesses.
2. Can the definition in of collision probabilities in [(Tengesdal et al. 2020)] be adapted to more complex scenarios than pure straight-line motion? 
3. The difficulties with the approach in [(Tengesdal et al. 2020)] stem from representing the safety zone constraints in the initial state space. Explore how these can be represented. 
4. Write a survey on techniques that can be used for integrating a Gaussian over a non-trivial set of hard constraints. 
5. Identify a promising alternative to brute-force importance sampling and implement it. Analyze accuracy and computational demands. 
6. Write report.

## Proposed Tasks for the master thesis

The project work aims to be extended into a master thesis for the spring of 2020. Here, the ambition is to verify, improve and utilise the results from the specialisation project. The following tasks are suggested:

1. Probabilities cannot be arbitrary. If collision happens in 50 percent of the cases, and the collision probability never is larger than 0.01, then clearly something is wrong. How can you verify that the probabilities are meaningful in simulations? The challenge here is that the collision probabilities typically should be rather small. 
2. Once a framework is in place for verification, it may be worthwhile to strive for further improvements in accuracy and run-time. Keep in mind that very accurate evaluation may not be meaningful. 
3. Can the probabilities be used as input to an MPC-based COLAV method?
4. Should the traffic rules at sea (COLREGS) and other means for predicting the intentions of obstacle vessels be taken into account?

## Prerequisites

The candidate should have taken the course [TTK4250 Sensor fusion]  before this project, or take it in parallell. Additional courses in statistic, estimation or probability will be useful. 

## Autosit

The candidate will be associated with the [AUTOSIT] project, 
which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics.
The goal of the [AUTOSIT] project is 
to deliver algorithms for situational awareness that enable autonomous surface vessels (ASVs) to guess and predict the intentions of other vessels. 
The [AUTOSIT] project is a direct successor of the [AUTOSEA] project, which focused on [sensor fusion and collision avoidance for ASVs]. 
A list of students who previous have written master theses on autonomous ship technology at NTNU can be found [here].

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)

## References

* Tengesdal, T.,  Brekke, E. and Johansen, T. A. (2020): [“On collision risk assessment for autonomous ships using scenario-based MPC”](https://folk.ntnu.no/torarnj/TTengesdal_2020_On_collision_risk_assessment_for_autonomous_ships_using_scenario_based_mpc.pdf), Proc. IFAC World Congress.

* Tengesdal, T., Johansen, T. A. and Brekke, E. (2022): [“Ship Collision Avoidance Utilizing the Cross-Entropy Method for Collision Risk Assessment”](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828), IEEE Transactions on Intelligent Transportation Systems.

* Johansen, T. A., Perez, T. and Cristofaro, A. (2016): [“Ship collision avoidance and COLREGS compliance using simulation-based control behavior selection with predictive hazard assessment”](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2469879), IEEE Transactions on Intelligent Transportation Systems, vol. 17 no. 12.

[AUTOSEA]: https://www.ntnu.edu/autosea/
[here]: https://folk.ntnu.no/edmundfo/autoseastudents/autoseastudents.html
[AUTOSIT]: https://www.ntnu.edu/autosit
[the sensor fusion book]: http://folk.ntnu.no/edmundfo/msc2019-2020/sf13chapters.pdf
[TTK4250 Sensor fusion]: http://folk.ntnu.no/edmundfo/msc2019-2020/sf13chapters.pdf
[(Tengesdal et al. 2020)]: https://folk.ntnu.no/torarnj/TTengesdal_2020_On_collision_risk_assessment_for_autonomous_ships_using_scenario_based_mpc.pdf
[(Johansen et al. 2016)]: https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2469879
[(Tengesdal et al. 2022)]: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828