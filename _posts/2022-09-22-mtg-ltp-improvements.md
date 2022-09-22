---
layout: post
title: Joint destination and kinematics prediction
category: LTP
---
## Background

|<img src="{{site.url}}/assets/mg_w_ais_density3-eps-converted-to.pdf" width="750" > |
| <span style="color:#959595">A maritime traffic graph representation of AIS data [(Tengesdal et al. 2022)]. </span> |

When a larger vessel enters the Trondheimsfjord, there is a limited finite number of possible destinations it can consider. It is natural that knowledge on the intended destination for the vessel will help in predicting its future trajectory. All passenger ships, ships carrying 500+ gross tonnage, and ships carrying 300+ gross tonnage during international voyage are obliged to use an Automatic Identification System (AIS) transponder.

In [(Tengesdal et al. 2022)] a maritime graph was created to represent traffic patterns in the Trondheimsfjord based on historical AIS data from the area, and used in a method for jointly inferring the kinematics (position, velocity) and destination of a vessel. The method uses an Ornstein-Uhlenbeck process [(Millefiori et al. 2016)] to predict the vessel trajectory along the maritime graph. When the prediction reaches a graph node which is closest to a considered destination, a so-called bridge model is used to predict the vessel convergence towards the destination. A challenge here is that it can be hard to tune and configure this bridging model to correctly estimate the arrival time of the vessel.

Furthermore, the method only captures the vessel behavior on the maritime traffic graph, whereas off-pattern behavior not captured by the majority of AIS data is not considered. Here, it would be very beneficial to consider also the vessel type when predicting its behavior. Where cargo ships mostly adhere to regular patterns with constant speed and a fixed course changes at typical turning points, recreational vessels with AIS transponders will typically maneuver to a larger degree about and off these regularized patterns.

|<img src="{{site.url}}/assets/maritime_graph_easier-eps-converted-to.pdf" width="750" > |
| <span style="color:#959595">Illustration of the prediction method in [(Tengesdal et al. 2022)]. </span> |

## Scope

The main goal of the project is to improve the arrival time estimation in the mentioned long-term prediction method, and possibly extend the method to take into account off-pattern vessel behavior, vessel ship type etc.

## Proposed Tasks for the 5th year project

The focus in the 5th year project shall be on exploring the collision probability problem. The following tasks and research questions should be addressed.

1. Write a survey on long-term prediction methods that incorporate extra information such as knowledge on possible destinations, traffic patterns, ship types etc., by searching the scientific literature. Discuss assumptions, approximations, strengths and weaknesses of the surveyed methods.
2. Use an existing implementation of the method [(Tengesdal et al. 2022)] or from scratch if preferable, become familiar with the method`s strengths and weaknesses.
3. Suggest improvements/changes in the method [(Tengesdal et al. 2022)] to make the vessel arrival time estimation better, and possibly also the prediction accuracy.
4. Compare the method with your suggested improvements against existing state of the art methods (some implementations of these are already given), on real AIS data.
5. Write report/paper.

## Proposed Tasks for the master thesis

The project work aims to be extended into a master thesis for the spring of 2023. Here, verification and utilization of the results from the specialization project will be central.

- Create a long-term prediction benchmark from AIS data, consisting of a selection of different vessel trajectories to consider.
- Suggest ways of taking into account off-pattern behavior in the prediction method. Can the type of vessel be incorporated here?
- Incorporate the method in a long-term collision avoidance (COLAV) framework such as the PSB-MPC [(Tengesdal et al. 2022b)] (code exists)
- Test the COLAV system on historical AIS data
- Design of new MPC-based COLAV methods capable of using collision probabilities or related risk measures in a meaningful way.

## Prerequisites

The candidate should have taken the course [TTK4250 Sensor fusion]  before this project, or take it in parallell. Additional courses in statistic, estimation or probability will be useful.

## Contact

For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo) or co-supervisor [Trym Tengesdal](https://www.ntnu.no/ansatte/trymte)

## References

- Tengesdal, T., Millefiori, L. M., Braca, P. and Brekke, E. (2022): [“Joint Stochastic Prediction of Vessel Kinematics and Destination based on a Maritime Traffic Graph”], Proc. of the International Conference on Electrical, Computer, Communications and Mechatronics Engineering  (ICECCME), 16-18 November 2022, Maldives, In press.

- Tengesdal, T., Johansen, T. A. and Brekke, E. (2022): [“Ship Collision Avoidance Utilizing the Cross-Entropy Method for Collision Risk Assessment”](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828), IEEE Transactions on Intelligent Transportation Systems.

- Millefiori, L. M., Braca, P., Bryan, K., and Willett, P., ["Long-term vessel kinematics prediction exploiting mean-reverting processes"](https://ieeexplore.ieee.org/document/7527893) in 2016 19th International Conference on Information Fusion (FUSION), Jul. 2016, pp. 232-239.

[TTK4250 Sensor fusion]: http://folk.ntnu.no/edmundfo/msc2019-2020/sf13chapters.pdf
[(Tengesdal et al. 2022a)]:
[(Tengesdal et al. 2022b)]: <https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508828>
[(Millefiori et al. 2016)]: <https://ieeexplore.ieee.org/document/7527893>
