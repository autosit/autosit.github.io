---
layout: post
title: World Picture for Maritime Collision Avoidance
subtitle: Visualization and Situation Awareness
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. A key objectives of the project is to involve sensor fusion so that vehicles are able to perceive the environment, and thus rely on such human-like sensing in addition radio communication and transponder systems, which may or may not be availabe. Furthermore, the general architecture of information flow in collision avoidance systems is also a topic of study in the project. 


## Scope
Collision avoidance is quite complex compared with many other cybernetical systems. While path planning, guidance and control of vehicles are largely solved problems, the synthesis of reactive collision avoidance with these tasks is not trivial, and does not easily lend itself to stability proofs and other conventional control theoretic analysis techniques. For example, when several vehicles interact, whether manned or autonomous, mutual misunderstandings of behavior can lead to dangerous situations. Sensor fusion adds another layer to the complexity. In real life, a collision avoidance system must make decisions based on incomplete and possibly faulty information, as the sensors may fail to detect obstacles, or mistake noise and clutter for real obstacles. In brief, the collision avoidance system must exhibit what is known as situation awareness. 

In order to keep the human in the loop, it is necessary to extract and present the essentials of this information in a meaningful manner. What is essential and meaningful may depend on the situation and the intentions of the operator. For a remote operator, limited bandwidth may be an issue, and one must then prioritize which information should be transferred to the operator. Presentation of information is also important during the development of simulators for collision avoidance. To investigate the behavior of collision avoidance methods, responding to various sensor input, researchers should be able to display sensor data, corresponding tracking and navigation results, and various collision avoidance concepts such as planned paths and velocity obstacles on-demand when this is considered useful. 

The main purpose of this project is to develop a visualization toolbox to be used in simulations of sensor fusion and collision avoidance in the Autosea project. 

## Proposed Tasks

1. Perform a litterature review over recent advances in situation awareness for (maritime) collision avoidance.
2. Identify key concepts that should be visualized. 
3. Identify metrics of danger etc. that can provide situation awareness. 
4. Implement the tools in a simulator based on the Robotic Operating System. This will be done in close collaboration with the Ph.D. candidates working on the Autosea project.
5. Discuss to which extent the visualizations provides adequate situation awareness.

## Prerequisites
This is a list of *recommended* prerequisites for this master project.

- Strong programming skills. Experience with ROS will be very advantageous.
- Knowledge of Kalman filtering.
- Knowledge of guidance and navigation of surface vehicles.

## Contact
For more information, contact main supervisor Edmund F. Brekke (<edmund.brekke@itk.ntnu.no>).
