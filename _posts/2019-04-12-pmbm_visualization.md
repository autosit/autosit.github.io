---
layout: post
title: Visualization and situational awareness for the PMBM filter
category: SF
---
## Background

Multi-target tracking is a crucial component of situational awareness systems for autonomous ships. 
Historically, the gold standard for multi-target tracking has been variations of the Multiple Hypothesis Tracker (MHT), 
which attempt to enumerate all possible data association hypotheses so that the best hypothesis can be found, and then uses Kalman filtering 
to estimate kinematics of the targets conditional on such hypotheses. 

A more refined version of MHT known as the Poisson Multi-Bernoulli Mixture (PMBM) filter has recently emerged with basis in the theory of random finite sets. 
PMBM has a more economical hypothesis representation than conventional MHT, and has stronger optimality properties. 
However, state-of-the-art PMBM implementations have not yet reached the same maturity as established MHT implementations. 

A goal in the Autoferry project is to develop a multi-sensor PMBM tracker that will form the backbone of Milliampere's sensor fusion system. 
In the Autosit project, the PMBM formalism will be used as a foundation for radar-AIS fusion. 
To enable these ambitions it is extremely important to have a sufficient arsenal of functions to visualize what goes on inside the multi-target tracker. 
This can quickly lead into deep fundamental questions, such as how the user interface should decide which out of several conflicting hypotheses are to be displayed to a human operator. 

|<img src="{{site.url}}/assets/whyClusterSplittingIsNeeded.png" width="620"> | 
| Simulation results for a PMBM implementation where high-quality tracks are seen to form limited clusters, while including the low-quality tracks leads to one big cluster.  |

## Scope

During this assignment, the candidate will become familiar with implementations of PMBM under development in Matlab or Python. 
The main goal is not primarily to further develop these methods, but to construct functions to that makes it easy for a human operator to understand how these implementations operate. 
A secondary goal is to consider different possibilities for how their output should be processed in order to be used as input in a collision avoidance system. 


## Proposed Tasks for the 5th year project

In the specialization project the main focus will be on a track display for PMBM. The following tasks are proposed for the specialization project:

* Make yourself familiar with multi-target tracking, random finite sets, MHT and PMBM. 
* Write a survey on existing research on visualization of multi-target tracking.
* Suggest a handful of output representations from the PMBM filter, and discuss their potential utility and reliability. Such representations can be the tracks of the top hypotheses, multi-target versions of maximum a posteriori estimates, occupancy grids, etc. 
* Implement functions to obtain the chosen output representations, and experiment with graphical effects (e.g., coloring) to convey the information in the best possible way. 
* Test the utility of the developed functions as part of PMBM tracking in simulations and on real data from the Autosea and Autoferry projects.
* Write report and discuss the findings in the report. 

## Proposed Tasks for the master thesis

In the MSc thesis the candidate will aim to further expand the work from the specialization project into a system for situational awareness. The context of situational awareness applies both to a human operator overseeing the autonomous system, and collision avoidance methods that use the PMBM results as input. Several variations are possible, depending on the interests of the candidate. 

* Experiment with closed-loop usage of the tracking system as part of a COLAV system in simulations. This approach will involve collaboration with one or more of the PhD students who currently work on maritime COLAV at ITK.
* Investigate more carefully how accurate different output representations really are. Which measures can we use to quantify this?
* Expand the work from the specialization project to handle heterogeneous multi-sensor tracking, e.g., fusion of cameras and radar. 
* Test the visualization systems on trained operators and compare with professional ARPA displays. 

This project can be expanded into a PhD or integrated PhD for a candidate with sufficient skills, background knowledge and motivation. 

## References
Williams, J. (2015). "[Marginal multi-Bernoulli filters: RFS derivation of MHT, JIPDA, and association-based member.][Williams2015]" IEEE Transactions on Aerospace and Electronic Systems, vol. 51, no. 3.

Crouse, D., Willett, P. and Bar-Shalom, Y. (2011). "[Developing a Real-Time Track Display That Operators Do Not Hate.][Crouse2011]" IEEE Transactions on Signal Processing, vol. 59, no. 7.

## Contact

Supervisor: [Edmund Brekke].  

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Williams2015]: https://ieeexplore.ieee.org/document/7272821
[Crouse2011]: https://ieeexplore.ieee.org/document/5740994