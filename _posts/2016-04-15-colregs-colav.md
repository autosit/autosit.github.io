---
layout: post
title: Collision avoidance for ASVs focusing on COLREGS
---
Autonomous technology is spreading across numerous applications at an unprecedented pace. Amongst others, the DARPA Grand Challenge for autonomous ground vehicles has given an indication of what is possible to achieve using state-of-the-art sensors in combination with cleverly designed autonomous algorithms. We believe the increasing use of autonomy in vehicle systems eventually will propagate to the maritime industry and that we will see an increasing level of autonomy on ships in order to increase safety, and to reduce operational costs, emissions and impacts from human-induced errors.

When designing control systems for autonomous surface vehicles (ASVs), and particular in the design of collision avoidance (COLAV) functionality, the international regulations for preventing collisions at sea (COLREGS) must be considered. COLREGS was introduced in the late 19th century, and has been revised multiple times as technology and methods have advanced. The rules have, however, not been adapted to facilitate autonomous vessels. Evaluating which parts of COLREGS should apply in different scenarios is therefore a necessity in order to develop autonomous COLAV.

This proposal is intended as a combined project and master thesis during the autumn of 2016 and spring of 2017. The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

| <img src="{{site.url}}/assets/mariner.jpg" width="370"> | | <img src="{{site.url}}/assets/telemetron4a.jpg" width="370"> |
|:---:| :---: |:---:|
| USV Mariner, an unmanned surface vehicle | | MR Telemetron, a dual-use surface vessel |

## Proposed Tasks
**For the project assignment (autumn 2016), the following tasks are proposed:**

1. Do a literature review on COLREGS. Look into its suitability, and how it has been applied so far, for ASVs. The literature review should also include collision avoidance (COLAV) algorithms for ASVs.
2. Implement a simulation framework to simulate different scenarios, with the possibility of including both static and moving obstacles.
3. Implement some suitable COLAV algorithms, and start working on an algorithm for deciding which parts of COLREGS applies in given scenarios.

**For the master thesis (spring 2017), the following tasks are proposed:**

1. Design an algorithm to decide which parts of COLREGS applies in given scenarios. This involves quantifying COLREGS into measurable concepts of closest point of approach (CPA), time until CPA (TCPA), relative bearings, etc.
2. Which rules are best suited to be acted upon by respectively deliberate and reactive COLAV algorithms?
3. Combine the designed algorithm with deliberate and reactive COLAV algorithms, through a suitable interface. 
4. Evaluate the performance of the COLREGS-interpreting algorithm and the overall system through simulations.
5. Based on the simulation results, full-scale tests may be possible.

## Supervisors 
Main supervisor: [Morten Breivik](http://www.ntnu.no/ansatte/morten.breivik). <br />
Co-supervisors: [Bjørn-Olav H. Eriksen](http://www.ntnu.no/ansatte/boerikse) and [Øystein Engelhardtsen (DNV-GL)](mailto:Oystein.Engelhardtsen@dnvgl.com)