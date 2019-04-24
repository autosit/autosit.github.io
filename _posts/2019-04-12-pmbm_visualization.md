---
layout: post
title: Visualization for the PMBM filter
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

## Scope

During this assignment, the candidate will become familiar with implementations of PMBM under development in Matlab or Python. 
The main goal is not primarily to further develop these methods, but to construct functions to that makes it easy for a human operator to understand how these implementations operate. 
A secondary goal is to consider different possibilities for how their output should be processed in order to be used as input in a collision avoidance system. 


## Proposed Tasks for the 5th year project

During the project period the candidate will perform a literature review of system identification techniques and experiments, familiarize themselves with the lab and the available tools, as well as write a report containing their findings.
Time permitting, the candidate will also work on the following suggested objectives for a continuation towards a master's thesis:
* Create an accurate mathematical model of the dynamics of one of the depicted ships.
* Create an accurate mathematical model of the ship's actuators.
* Verify and validate the model using simulation and experiments.
* Create ship controllers for course and speed.
* Verify and validate the performance of these controllers experimentally.

## Proposed Tasks for the master thesis

bla bla


## References
[Williams, J. (2015). "Marginal multi-Bernoulli filters: RFS derivation of MHT, JIPDA, and association-based member." IEEE Transactions on Aerospace and Electronic Systems, vol. 51, no. 3.][Williams2015]  

## Contact

Supervisor: [Edmund Brekke].  

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Williams2015]: https://ieeexplore.ieee.org/document/7272821