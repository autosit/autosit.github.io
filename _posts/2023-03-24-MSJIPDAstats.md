---
layout: post
title: Towards accurate Multi-sensor object tracking
category: SF
---
## Background
Researchers at NTNU are currently developing an autonomous ferry designed for carrying pedestrians and cyclists between Ravnkloa and Brattøra. The development of a robust collision avoidance system for this ferry relies on having an accurate multi-sensor (MS) multi-object tracking (MOT) system using radar, lidar, optical cameras, and infrared cameras. The MS MOT again needs an accurate model of the environment and its sensors. More specifically there is a need for a thorough understanding of the number of vessels and kayaks in the region with their behavior pattern, as well as sensor true/false positives rates.

There is also a lack of standardized tools to assess the validity of chosen models and parameters. New tools could be different confidence intervals on the observed data, for example. Having better and more standardized tools could help ensure the accuracy of the MS MOT.

![Brattøra]({{site.url}}/assets/brattora.jpg)

## Scope
The goal of this project is to investigate what is the proper models and parameters to use in an MS joint integrated probabilistic data association (JIPDA) (Helgesen et al., 2022). The candidate will develop and integrate new models with our MS JIPDA tracker and analyze several datasets. In addition, they will be a part of developing and testing new tools for assessing the validity of the model and parameters.


## Proposed Tasks
1. Implement and test one or more of the following models in an MS JIPDA on our datasets from the canal.
   1. Spatially varying new object intensity (number of vessels)
   2. Dynamic model based on common routes/maneuvers, etc. (vessel behavior)
   3. Spatially varying clutter intensity for one or more of the sensors(false positive rates)
   4. Spatially varying detection probability for one or more of the sensors (true positive rates)
2. Develop/test one or more parameter validity metrics/statistics.
3. Assess the methods against simpler ones for real-time tracking.

These tasks can be performed as a collaboration between multiple candidates if preferred.

The scope of the specialization project will be to investigate one of the models and assess it with one preliminary validity metric. The master thesis will then look at more models or more and better metrics, or a combination.

## Supervisors
Main supervisor: [Edmund Brekke](http://www.ntnu.no/ansatte/edmund.brekke).<br>
Co-supervisor: [Lars-Christian Ness Tokle](https://www.ntnu.no/ansatte/lars-christian.n.tokle).<br>

## References
- (Helgesen et al., 2022): Øystein Kaarstad Helgesen, Kjetil Vasstein, Edmund Førland Brekke, Annette Stahl, ["Heterogeneous multi-sensor tracking for an autonomous surface vehicle in a littoral environment"](https://www.sciencedirect.com/science/article/pii/S0029801822005753), Ocean Engineering, Volume 252, 2022.
