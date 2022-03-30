---
layout: post
title: Multi-sensor extended object tracking
category: Nonsense
---
|<img src="{{site.url}}/assets/nidarholmdata.png" width="700"> | 
|<span style="color:#959595"> The ferry MS Nidarholm maneuvering out of its quay position as seen in lidar data (different colors are different time steps). The goal of extended object tracking is to estimate its position, velocity, shape and orientation from these data. Based on Ruud et al. (2018). </span>| 

## Background

Situational awareness (SITAW) for an autonomous vehicle (e.g., autonomous ship) depends on sensors that can perceive obstacles and other vehicles, 
and track and predict their motion so that collisions are avoided. 
Popular sensors include maritime radar, lidar, optical cameras and infrared cameras. 

Traditional maritime SITAW systems have been centred around the maritime radar, which is the only reliable sensor when the sensing system must cover several kilometers on the open sea. However, on shorter ranges lidars and cameras can provide richer information, which can be of crucial importance when margins of errors are smaller due to increased congestion or more confined environments (e.g., in harbours). Both in lidar data and in camera data it is possible to make inference about the shape and extent of other boats. 

While the traditional tracking methods from the 70s and 80s have assumed that all targets are points, more recent methods for extended object tracking (EOT) attempt to estimate the shapes of the targets. This is an active research area, which has not yet arrived at the same maturity as traditional tracking methods.  Key challenges include the following:

* Different parametrizations of of extent are possible. These include [random matrices], [ellipses] or more general [star-convex shapes], [Gaussian processes], etc. All come with different strengths and weaknesses, and are in general nontrivial to work with. 
* A multi-target EOT method should ideally consider all plausible [partitions] of the data into different combinations of extended objects. This leads to a data association problem that is much more complex than for traditional multi-target tracking. 
* Measurement models rely on questionable approximations (e.g., random matrices or Gaussian processes for lidar) or it may not even be clear how a measurement model should be formulated (for EOT based on cameras). 
* It is difficult to make a good [process model] that accounts for the subtle correlations between orientation and velocity. 

|<img src="{{site.url}}/assets/gpeot.jpg" width="700"> | 
| <span style="color:#959595">Gaussian process EOT parametrization from Lopez (2019). </span>| 

Nevertheless, the time may be ripe for a breakthrough in maritime extended object tracking. There are reasons to be optimistic and ambitious:

* Significant progress on EOT has been made by handful of research groups, in particular at Chalmers University in Sweden. This includes a [integration of EOT] in the [Poisson Multi-Bernoulli Mixture (PMBM)] framework, which is the de facto gold standard for multi-target tracking. 
* The related problem of [simultaneous localization and mapping (SLAM)] has been extensively researched over the last decade. It may be possible to adapt techniques from SLAM to EOT (e.g., pose graph optimization).
 
## Scope

The goal of this combined specialization and MSc project is to develop an EOT algorithm that combines data from an active sensor (lidar) with data from a passive sensor (infrared or optical camera). 

|<img src="{{site.url}}/assets/SimEigen.png" width="700"> | 
|<span style="color:#959595"> Point cloud reconstruction of milliAmpere2 from monocular camera simulation in the Gemini Autoferry simulator. Based on Lauvsnes (2019).</span>| 

## Proposed Tasks for the 5th year project

The following tasks are proposed for the specialization project:

* Data consolidation. Do interesting data exist? Make experiments or use the [Gemini Autoferry simulator].
* Synchronization and calibration. 
* Literature review: Investigate relevant techniques, including different EOT algorithms, alternative pose estimation techniques (ICP, PCA) and structure-from-motion approaches. 
* Problem formulation: Identify missing building blocks in the above “lego collection”, and suggest possible fusion architectures. 
* Implement a scheme for multi-sensor joint tracking and pose estimation.  

## Proposed Tasks for the MSc thesis

In the MSc thesis the goal will be to integrate the work from the specialization project into the framework of multi-target tracking. 

* Conduct a literature survey on the most popular and relevant approaches to multi-target tracking. 
* Define a suitable state representation and motion model based on the findings from the specialization project. 
* Formulate measurement models for the sensors involved, so that Bayesian state estimation can be used. 
* Implement a Bayesian filter for the single-target multi-sensor EOT problem. 
* Include models for clutter, misdetections and multi-target association uncertainty. 
* Implement a multi-target multi-sensor EOT method. 

## Prerequisites

Useful courses include [TTK4250 Sensor fusion], TTK21 VSLAM, TTK25 Computer Vision for Control  and TTK4255 Robotic Vision. The candidate should have taken some of these already, and take some of the remaining courses in parallell with the specialization project. 

## References
* Granström, K., Baum, M. and Reuter, S. (2017). "<a href="http://isif.org/journal/12/2/1557-6418">Extended Object Tracking: Introduction, Overview and Applications.</a>" Journal of Advances in Information Fusion.
* Granström, K., Fatemi, M. and Svensson, L. (2020). "<a href="https://ieeexplore.ieee.org/document/8730493">Poisson multi-Bernoulli mixture conjugate prior for multiple extended target filtering.</a>" IEEE Transactions on Aerospace and Electronic Systems.
* Ruud, K., Brekke, E., & Eidsvik, J. (2018): “[LIDAR Extended Object Tracking of a Maritime Vessel Using an Ellipsoidal Contour Model](https://www.researchgate.net/publication/328890666_LIDAR_Extended_Object_Tracking_of_a_Maritime_Vessel_Using_an_Ellipsoidal_Contour_Model)”, SDF 2018.
* Kamsvåg, V. (2018). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/kamsvaag_msc.pdf">Fusion between camera and lidar for autonomous surface vehicles.</a>" MSc thesis, NTNU.
* Lopez, E. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/lopez_eot.pdf">LIDAR Extended Object Tracking of a Maritime Vessel using Gaussian Processes.</a>" Specialization project, NTNU. 
* Lauvsnes, M. (2019). "<a href="http://folk.ntnu.no/edmundfo/msc2019-2020/lauvsnes_pose_estimation.pdf">Detection and pose estimation by
means of synthetic camera data.</a>" Specialization project, NTNU.



## Contact

Supervisors: [Edmund Brekke], [Annette Stahl] and [Rudolf Mester]


[Edmund Brekke]: https://www.ntnu.edu/employees/edmund.brekke
[Annette Stahl]: https://www.ntnu.edu/employees/annette.stahl 
[Rudolf Mester]: https://www.ntnu.edu/employees/rudolf.mester
[ellipses]: https://www.researchgate.net/publication/328890666_LIDAR_Extended_Object_Tracking_of_a_Maritime_Vessel_Using_an_Ellipsoidal_Contour_Model
[random matrices]: https://ieeexplore.ieee.org/abstract/document/4655362
[star-convex shapes]: https://ieeexplore.ieee.org/document/6809906 
[Gaussian processes]: https://ieeexplore.ieee.org/document/7088657
[partitions]: https://ieeexplore.ieee.org/document/7995696
[process model]: https://ieeexplore.ieee.org/document/6850178
[Poisson Multi-Bernoulli Mixture (PMBM)]: https://ieeexplore.ieee.org/document/7272821
[integration of EOT]: https://ieeexplore.ieee.org/document/8730493
[simultaneous localization and mapping (SLAM)]: https://www.cs.cmu.edu/~kaess/pub/Kaess12ijrr.pdf
[Gemini Autoferry simulator]: http://folk.ntnu.no/edmundfo/msc2020-2021/eitdigtwin.pdf
[TTK4250 Sensor fusion]: http://folk.ntnu.no/edmundfo/msc2019-2020/sf13chapters.pdf