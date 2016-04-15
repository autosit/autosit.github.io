---
layout: post
title: Collision Avoidance System for Ships Utilizing Other Vessels' Intentions
[//]: # subtitle: Visualization and Situation Awareness
---
![Collision Avoidance]({{site.url}}/assets/intention_1.png)![Collision Avoidance]({{site.url}}/assets/intention_2.png)

Over the last decades, several new sensors and systems have been introduced on ships to improve navigational safety, for example GPS, AIS (Automatic Identification System) and ECDIS (electronic maps). Despite such advances collisions and groundings are still two of the most frequent causes of maritime accidents.

When it comes to collision avoidance, the challenge for the navigator on the bridge is not only to understand and operate navigational systems onboard his own vessel, but also to interpret other vessel’s movements and to steer the vessel according to the traffic rules of the seas (COLREG). Velocity Obstacle (VO) is a promising algorithm for avoiding collisions with moving vessels with a constant velocity vector. (ref Thomas Stenersen’s Master thesis, June 2015). However, the VO algorithm is naive because in reality other vessels are dynamically steered by a human navigator or in the case of an unmanned vessel, a control algorithm.

The task of this assignment is to design a navigational guidance system which utilizes a priori information about other vessels’ intentions or near-future route plans, and assess the potential improvement over a more naive algorithm such as VO. The navigational guidance system may be used as decision support to the navigator on a manned vessel, but could also be used for controlling an unmanned, autonomous surface vehicle (ASV).

The guidance system can assume a sensor package and a priory chart data to provide a sufficient picture of the ships’ surroundings in order to navigate safely. The system should be able to plan and execute safe route avoiding collisions with other vessels but also avoid grounding with fixed obstacles such as archipelago. The system shall also be able to act according to international regulations at sea (COLREGS).

## Proposed Tasks
For the project assignment, the following tasks are proposed:

1. Do a literature survey on collision avoidance for surface vessels and assess the properties of different approaches for collision avoidance. Consider how other vessels’ intentions could be exploited to reduce collision risk.  
2. Design and implement a collision avoidance system capable of navigating safely in various types of waters, and to act on suddenly occurring obstacles, as well as utilizing other vessels intentions
3. Create a simulator for the vessel, the environment and other vessels and demonstrate the capabilities of the developed system.

For the master thesis, the following tasks are proposed:

1. Do a literature survey on navigational sensors, navigational regulations (COLREGs), and guidance systems for autonomous surface vehicles (ASV). 
2. Study how ships are manually operated to avoid collisions:
    * Identify the most critical situations and the main reasons for collisions.
    * Identify traditional maneuvers to avoid collisions.
    * How do navigators agree on solving situations?
3. Devise a scheme for utilizing other vessels’ intentions (e.g. near-future route plan or rate of turn) as a priori information to improve the collision avoidance system and consider a suitable vessel-to-vessel communication method to support the concept (e.g. AIS, Satellite communications or visual indications).
4. Design a navigational guidance system capable of navigating safely in various types of waters, and to act on suddenly occurring obstacles
    * Develop/refine a collision avoidance algorithm utilizing other vessels intentions.
    * Develop/reuse another reference collision avoidance algorithm based on a method which is not utilizing other vessels’ intentions (for example VO).
5. Create a simulator for the vehicle and the surroundings, and demonstrate the capabilities of the developed guidance system, and assess the improved collision avoidance ability resulting from utilizing other vessel intensions by considering typical sea traffic situations (e.g. head-on and crossings) as well as critical situations causing collisions between human operated vessels.

## Supervisors
Main supervisor: [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo), Associate Professor, NTNU

Co-supervisor: Steinar Låg, Principal Researcher, Maritime Transport, DNV GL - Strategic Research and Innovation
