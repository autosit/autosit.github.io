---
layout: post
title: HIL-testing for Maritime Collision Avoidance Systems
---

![Revolt]({{site.url}}/assets/revolt.jpg)

In 2013 the ReVolt was initiated as a research project by the Strategic Research and Innovation group at DNV GL. It was launched externally one year later and caught a lot of attention by media around the world. The ReVolt is a shipping concept for the short-sea segment that offers a possible solution to the growing need for transport capacity. It does not require a crew and therefore goes a long way in tackling one of the shipping industries’ weakest links: the safety record. With an average of 900 fatalities per year the mortality rate in shipping is 10 times higher than in comparable land-based industries. Studies have shown that the majority of these accidents are caused by human error. Unmanned vessels take this factor out of the equation and make the operation of these ships more cost-efficient.

The team behind the ReVolt is now looking further into the technologies that someday may enable unmanned shipping and is currently working on forming requirements to ensure safe operation of such systems. Although the risk and consequences of human errors has the potential to be greatly reduced by the introduction of autonomous systems, this concept also brings with it a set of novel and largely unproven technologies that will introduce new and partly unknown sources of errors. These sources and the associated risks must be properly assessed. It is a common understanding that autonomous ships must be “as safe – or safer” than human operated ships in order to be accepted by the general public and put into operation. It is therefore expected that one of the largest hurdles along the way towards unmanned shipping will be the ability to provide credible assessments of safety and performance without having a sufficient record of systems in operation.   

![HIL setup]({{site.url}}/assets/hil_setup.jpg)

The use of simulations to verify and assure systems has gained popularity over the last decades as more and more complex systems are produced. Today, hardware-in-the-loop simulations are commonly used to verify performance and to ensure that all relevant combinations of errors are handled properly. This is used for many different applications and in several industries and is often the most effective way to uncover errors that occur only in specific cases. In a simulated environment, large amounts of scenarios can be tested without much effort. In the case of Dynamic Positioning systems for oceangoing vessels, DNV GL has formed specific requirements that are based on simulator verification (HIL testing). This is used to assure safety and performance of these systems before they are put into operation. The concept of verification through simulations is considered highly relevant also for future autonomous navigation- and specifically collision avoidance systems. 

The task of this assignment is to design and implement a simulated environment, able to verify performance of different collisions avoidance systems for ships. The task includes the implementation of several strategies for collision avoidance that will be assessed against developed requirements. This project is intended as a combined project and master thesis (autumn 2016 and spring 2017). The candidate will be associated with the AUTOSEA project, which is a collaboration project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused at attaining world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV.

## Proposed Tasks
For the project assignment, the following tasks are proposed:

1. Do a literature survey on autonomous surface vessels (ASV), and describe the properties of state-of-the-art approaches for collision avoidance
2. Design a guidance system for an ASV capable of navigating safely in various types of waters, and to act on suddenly occurring obstacles.
3. Interface the collision avoidance system to the DNV GL vessel simulator infrastructure<sup>\*</sup> developed for HIL testing by Marine Cybernetics
4. Implement simulation of other objects and vessels within this framework and demonstrate the capabilities of the developed system.

For the master thesis, the following tasks are proposed:

1. Do a study on how navigational regulations (COLREGs) are applied in practice and how ships are manually operated to avoid collisions:
    * Identify and list typical situations and the main reasons for collisions.
    * Identify traditional maneuvers to avoid collisions.
2. Develop a set of requirements based on this study that identifies important properties for a collision avoidance system.
3. Form a set of scenarios selected to test the developed requirements.
4. Develop a framework for the testing and verification of such systems, and implement this framework in the DNV GL system for automatic HIL testing<sup>\*</sup>. 
5. Implement several collision avoidance systems/algorithms and assess their performance in the simulated system based on the developed requirements. 

\*The DNV GL CyberSea simulator infrastructure includes various vessel models, environmental models and a toolbox for running and analyzing simulations. This also includes a system for automatic HIL testing and result assessment called Signature. Additional simulator models may be written in a number of programming languages or tools such as Simulink.

## Supervisors
Main supervisor: [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo), Associate Professor, NTNU

Co-supervisor: Steinar Låg, Principal Researcher, Maritime Transport, DNV GL - Strategic Research and Innovation
