---
layout: post
title: Automatic generation of maritime collision avoidance scenarios
category: COLAV
---
## Background
A key requirement for autonomous ships and autonomous surface vehicles (ASVs) is a safe and reliable collision avoidance (COLAV) system. Testing of such systems is challenging, because the system may in real life encounter a limitless number of different scenarios. To be able to test the system in a reasonable variety of scenarios, simulations are obviously needed. Such simulations can be conducted much more efficiently if hundreds and thousands of scenarios can be generated automatically.
 

## Scope
In this project the goal is to develop a simulator for generating a large number of geometric COLAV scenarios with various characteristics. These characteristics should include
- Different situations such as head-on, overtaking, being overtaken, crossing from right and left, etc. Such situations are often known as COLREGS situations. 
- How many vehicles are present, and their orientations, positions and velocities.
- Accuracy in the knowledge about other ships’ kinematic attributes.

It is important that the simulator strategically attempts to generate a variety of diverse scenarios, instead of merely making copies of the same scenario with insignificant variations. It is also important that the simulator produces scenarios of varying difficulty, so that the true limitations of COLAV methods can be discovered.

## Proposed tasks for the specialization project
1. Write a synopsis of the state of the art in maritime collision avoidance. 
2. Identify scenarios commonly tested in literature.
3. Identify design parameters that should be given as input to a scenario generator.
4. Identify performance measures that can be used to assess how difficult a scenario is and how well a COLAV method tackles it.
5. Outline a systematic recipe for generating scenarios.
6. Implement a program for generating scenarios.
7. Extend the program to include simulations with a chosen COLAV method.
8. Run simulations, and analyze performance measures with respect to design parameters and scenario characteristics.
9. Write report.

## Proposed tasks for the masters thesis

The project work aims to be extended into a master thesis for the spring of 2018. In the master thesis, a major aim will be to make the work more realistic. For example, constrains caused by land and by vehicles which may or may not follow COLREGS makes maritime collision avoidance a much more complex endeavour. Simulation techniques based on hardware-in-the-loop (HIL) testing can enable more realistic vehicle dynamics in the simulations. The scope of the master’s thesis will be discussed and outlined during the autumn 2017.

## Prerequisites
Required background knowledge:

- TTK 4190 Guidance and Control of Vehicles.
- Strong programming skills in Matlab, Python or C++.


## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Supervisors 
Main supervisor: [Edmund Brekke](http://www.ntnu.no/ansatte/edmund.brekke).

## References
Woerner, K. (2016): “[Multi-Contact Protocol-Constrained Collision Avoidance for Autonomous Marine Vehicles](https://dspace.mit.edu/handle/1721.1/104118)”, Ph.D. thesis, MIT.

