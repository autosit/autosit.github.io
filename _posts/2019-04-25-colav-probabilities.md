---
layout: post
title: Collision probabilities
category: LTP
---
## Background
Risk evaluations are an obvious component of a collision avoidance (COLAV) system. But what exactly is meant by risk? Is it a qualitative or a quantitative concept? We often think of risk as related to probability. This leads to the research question: Can we estimate the probability that a future collision will occur given some knowledge about the autonomous ship and other ships in its vicinity? 

In [(Tengesdal et al. 2020)] such probabilities were evaluated under an assumption of straight line motion. Importance sampling was used because the collision zone constraints necessarily are of a non-linear nature. See also Example 5.4 in Page 80 in [the sensor fusion book] for a more elaborate explanation. Since the random sampling leads to significant fluctuations, a Kalman filter was used to smoothen the probability estimates. The probabilities were used as input in the scenario-based model-prediction control (SB-MPC) COLAV method of [(Johansen et al. 2016)].

A slightly different approach was taken in [(Tengesdal et al. 2022)]. Here, an instantaneous collision probability was evaluated by integrating the target ship probability density function over the ownship safety zone. The Cross-Entropy method was used to implement a more efficient Importance sampler. However, the instantaneous interpretation is problematic if one wants to accumulate the probability of collision over several segments in a trajectory, because the sample time will affect the result. 

## Scope
The main goal of the project is to provide formulas or algorithms for reliable quantification of collision probability under sufficiently general circumstances to be of practical utility. 

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

The candidate should have taken the course [TTK4250 Sensor fusion]  before this project, or take it in parallell. Additional courses in statistic, estimation or probability will be useful. 

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)

## References

* Tengesdal, T.,  Brekke, E. and Johansen, T. A. (2020): [“On collision risk assessment for autonomous ships using scenario-based MPC”](https://folk.ntnu.no/torarnj/TTengesdal_2020_On_collision_risk_assessment_for_autonomous_ships_using_scenario_based_mpc.pdf), Proc. IFAC World Congress.

* Tengesdal, T., Johansen, T. A. and Brekke, E. (2022): [“Ship Collision Avoidance Utilizing the Cross-Entropy Method for Collision Risk Assessment”](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828), IEEE Transactions on Intelligent Transportation Systems.

* Johansen, T. A., Perez, T. and Cristofaro, A. (2016): [“Ship collision avoidance and COLREGS compliance using simulation-based control behavior selection with predictive hazard assessment”](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2469879), IEEE Transactions on Intelligent Transportation Systems, vol. 17 no. 12.


[the sensor fusion book]: http://folk.ntnu.no/edmundfo/msc2019-2020/sf13chapters.pdf
[TTK4250 Sensor fusion]: http://folk.ntnu.no/edmundfo/msc2019-2020/sf13chapters.pdf
[(Tengesdal et al. 2020)]: https://folk.ntnu.no/torarnj/TTengesdal_2020_On_collision_risk_assessment_for_autonomous_ships_using_scenario_based_mpc.pdf
[(Johansen et al. 2016)]: https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2469879
[(Tengesdal et al. 2022)]: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828