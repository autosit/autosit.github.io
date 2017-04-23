---
layout: post
title: World picture for maritime collision avoidance
category: SF
---
## Background

Collision avoidance is quite complex compared with many other cybernetical systems. While path planning, guidance and control of vehicles are largely solved problems, the synthesis of reactive collision avoidance with these tasks is not trivial, and does not easily lend itself to stability proofs and other conventional control theoretic analysis techniques. For example, when several vehicles interact, whether manned or autonomous, mutual misunderstandings of behavior can lead to dangerous situations. Sensor fusion adds another layer to the complexity. In real life, a collision avoidance system must make decisions based on incomplete and possibly faulty information, as the sensors may fail to detect obstacles, or mistake noise and clutter for real obstacles. In brief, the collision avoidance system must exhibit what is known as situation awareness.

An autonomous system should itself be prepared and able to react based on situation awareness, and it should also be able to convey the essential information of the situation to the human operator, who may or may not be required to interfere. The purpose of this autumn project is to design a collision warning system for ASVs based on these considerations. In the subsequent master thesis project, the aim will be to use the collision warning system actively. 

## Proposed Tasks
For the autumn project, the following tasks are proposed:

1. Perform a litterature review over recent advances in situation awareness for (maritime) collision avoidance.
2. Propose some risk measures to be used as part of a collision avoidance system.
3. Implement a collision warning system based on these measures. 
4. Develop visualization tools that can form part of a graphical user interface between the collision warning system and a human operator.
5. Discuss the findings in a report.

For the master thesis, the aim is to analyze the collision warning system in greater detail, and to extent it into a more comprehenive decision support system. The decision support system should be able to recommend different maneuvers to a human operator. 

The following topics should be addressed:

1. Discussion of the trade-off between false alarm rates and detection probabilities in a collision warning system.
2. Automatic suggestion of actions (maneuvers) to be considered by a human operator.
3. Detection of situations where another vehicle cannot be expected to follow COLREGS (e.g., because COLREGS does not apply, because its a rogue vehicle or because it is not under proper control).
4. Blind zones, bad weather impact,etc.
5. Assessment of multivehicle situations.

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
Main supervisor: [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo).<br />
Co-supervisors: Thor Hukkelås (Kongsberg) and Thomas Porathe. 
