---
layout: post
title: Navigational guidance system utilising other vessels’ intentions 
[//]: # subtitle: Visualization and Situation Awareness
---
Over the last decades, several new sensors and systems have been introduced on ships to improve navigational safety, for example GPS, AIS (Automatic Identifaction System) and ECDIS (electronic maps).   Despite such advances collisions and groundings are still two of the most frequent causes of maritime accidents. 

When it comes to collision avoidance, the challenge for the navigator on the bridge is not only to understand and operate navigational systems onboard his own vessel, but also to intreprete other vessel’s movements and to steer the vessel according to the traffic rules of the seas (COLREG). Velocity Obstacle (VO) is a promising algorithm for avoiding collsions with moving vessels with a constant velocity vector. (ref Thomas Stenersen’s Master thesis, June 2015). However, the VO algorithm is naive because in reality other vessels are dynamically steered by a human navigator or in the case of an unmanned vessel, a control algorithm. 

The task of this assignment is to design a navigational guidance system which utilizes a priori information about other vessels’ intentions or near-future route plans, and assess the potential improvement as compared to using a more naive algorithm such as VO. The navigational guidance system may be used as decision support to the navigator on a manned vessel, but could also be used for controlling an unmanned, autonomous surface vehicle (ASV).  

The guidance system can assume a sensor package and a priory chart data to provide a sufficient picture of the ships’ surroundings in order to navigate safely. The system should be able to plan and execute safe route avoiding collisions with other vessels but also avoid grounding with fixed obstacles such as archipelago.  The system shall also be able to act according to international regulations at sea (COLREGS). 

## Proposed Tasks

1. Do a literature survey on navigational sensors, navigational regulations (COLREGs), and guidance systems for autonomous surface vehicles (ASV).
2. Devise a scheme for utilizing other vessels’ intentions (e.g.near future route plan or rate of turn) as a priori information to improve the guidance system, and consider a suitable vessel-to-vessel communication method to support the concept (e.g AIS, Satellite communications or visual indications).  
3. Design a navigational guidance system capable of navigating safely in various types of waters, and to act on suddenly occurring obstacles  
- Develop a reference collision avoidance algorithm based on a method which is not utilizing other vessels’ intentions (for example VO) 
- Develop a modified algorithm utilizing other vessels intentions
4. Create a simulator for the vehicle and the surroundings, and demonstrate the capabilities of the developed guidance system, and assess the improved collision avoidance ability resulting from utilising other vessel intensions by considering typical sea traffic scenarious (e.g.head-on and crossings). 

## Supervisors

Main supervisor: Edmund F. Brekke (<edmund.brekke@itk.ntnu.no>), Associate Professor, NTNU

Co-supervisor: Steinar Låg, Principal Researcher, Maritime Transport, DNV GL - Strategic Research and Innovation
