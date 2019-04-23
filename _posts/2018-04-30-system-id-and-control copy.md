---
layout: post
title: System identification and control of model ship
category: COLAV
---
![Autonomous shuttle ferry]
![Model scale vessels]
![ReVolt]

Accurate ship models are hard to come by, and many nonlinear control approaches are dependent on rigorous descriptions of the ship dynamics.
A common approach for generating a mathematical model is to build a scaled ship model, perform system identification on that model, and scale up this mathematical representation using prime or bis nondimensional models [(Fossen, 2011)](#Fossen2011).

During this assignment, the candidate will familiarize themselves with system identification techniques, ship modeling and control.
They will work one of the depicted ship models and identify an accurate mathematical description of its dynamics.
Additionally, the candidate will develop controllers for the ship, and verify and validate their performance experimentally.

During the project period the candidate will perform a literature review of system identification techniques and experiments, familiarize themselves with the lab and the available tools, as well as write a report containing their findings.
Time permitting, the candidate will also work on the following suggested objectives for a continuation towards a master's thesis:
* Create an accurate mathematical model of the dynamics of one of the depicted ships.
* Create an accurate mathematical model of the ship's actuators.
* Verify and validate the model using simulation and experiments.
* Create ship controllers for course and speed.
* Verify and validate the performance of these controllers experimentally.

## References
[Eriksen, B. H. and M. Breivik (2017). "Modeling, Identification and Control of High-Speed ASVs: Theory and Experiments." In: *Sensing and Control for Autonomous Vehicles*. Ed. by T. I. Fossen, K. Y. Pettersen, and H. Nijmeijer. Springer International Publishing, pp. 407-431.][Eriksen2017]  
<a name="Fossen2011"></a>
[Fossen, T. I. (2011). *Handbook of Marine Craft Hydrodynamics and Motion Control*. Wiley-Blackwell.][Fossen2011]  
[Sonnenburg, C. R. and C. A. Woolsey (2013). "Modeling, Identification and Control of an Unmanned Surface Vehicle." In: *Journal of Field Robotics* 30.3, pp. 371-398.][Sonnenburg2013]

Supervisor: [Morten Breivik].  
Co-supervisor: [Glenn Bitar].

[Morten Breivik]: https://www.ntnu.no/ansatte/morten.breivik
[Glenn Bitar]: https://www.ntnu.no/ansatte/glenn.bitar
[Autonomous shuttle ferry]: {{site.url}}/assets/sysid-autonomous-shuttle-ferry.jpg
[Model scale vessels]: {{site.url}}/assets/sysid-model-scale-vessels-mc-lab.jpg
[ReVolt]: {{site.url}}/assets/sysid-revolt.jpg
[Eriksen2017]: https://doi.org/10.1007/978-3-319-55372-6_19
[Fossen2011]: https://doi.org/10.1002/9781119994138
[Sonnenburg2013]: https://doi.org/10.1002/rob.21452