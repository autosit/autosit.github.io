---
layout: post
title: A Ship Motion Control Concept Inherently Satisfying Actuator Constraints
category: MISC
---
## Background
When a ship sails on the sea, its autopilot system usually leads the ship along the desired course. Countless motion controllers and autopilots have been proposed over the year. However, many control algorithms found in the literature do not consider saturation constraints for the actuators. 

#![Adaptive control loop]({{site.url}}/assets/adaptive.png)

## Scope
The goal of this project work is to investigate a combination of dynamic window and nonlinear feedback control algorithms to handle actuator constraints.

## Proposed Tasks
1. Develop and implement a combination of dynamic window and nonlinear cascaded feedback control algorithms as a heading and speed controller for a ship in Mat- lab/Simulink to address the problem of both magnitude and rate saturations for the actuators.to address the problem of both magnitude and rate saturations for the actuators. 
2. Perform a literature study on state-of-the-art constraint handling control methods.
3. Extend the dynamic window algorithm to three degree of freedom.
4. Develop and implement a combination of dynamic window and nonlinear cascaded feedback control algorithms as a motion controller for a ship in Matlab/Simulink to address the problem of both magnitude and rate saturations for the actuators.
5. Combine a selection of constraint handling control algorithms from the literature study with the nonlinear feedback controllers, to handle actuator constrains.
6. Compare the closed-loop performance of the combined control algorithms using performance metrics.

The project work aims to be extended into a master thesis for the spring of 2018. While the project goal is to get an overview of existing solutions, and test and compare these solutions through simulations in Matlab/Simulink, the master thesis goal is then to further develop and implement new methods, and perhaps test and compare these through both simulations and using model-scale ships in the Marine Cybernetics labo- ratory, see http://www.ntnu.no/imt/lab/cybernetics.

Specifically, the project work is suggested to be **extended into master thesis work during the spring of 2018**, including the following tasks:
1. Further develop the control algorithms from the project work such that they handle actuator constrains in an energy-efficient manner.
2. Implement and compare a newly proposed control algorithm with the previously tested algorithms in Matlab/Simulink.
3. If possible, test the performance of the algorithms in in model-scale experiments in the Marine Cybernetics laboratory.

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Supervisors 
Main supervisor: [Morten Breivik](http://www.ntnu.no/ansatte/morten.breivik).
Co-supervisors: [Mikkel Sørensen](http://www.ntnu.no/ansatte/mikkelns) and [Bjørn-Olav Eriksen](http://www.ntnu.no/ansatte/boerikse).
