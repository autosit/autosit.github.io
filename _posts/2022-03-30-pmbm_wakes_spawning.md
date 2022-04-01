---
layout: post
title: The PMBM filter 3 -  Beyond the standard model
category: SF
---
## Background

Methods for multi-target tracking in maritime and military applications are typically based on a common set of model assumptions, which can be called the standard model (page 137 in [Fundamentals of Sensor Fusion]). In particular, two aspects of the standard model are worth mentioning. First, it invokes the at-most-one assumptions, which says that maximally one measurement comes from each target, and that at most one target can be the source of any measurement. Second, it invokes several independence assumptions. Both false alarms and new targets are according to the standard model independent of the previously existing targets. 

There are, however, many real-world applications where these assumptions fail to hold. An example is ship wakes in maritime tracking. Measurements from the wake are of limited use in estimating the state of the boat, and are therefore discarded as clutter. But since the wake always is behind the boat, there is a dependency between the wake and the target state that violates the standard model. 

|<img src="{{site.url}}/assets/ais_slide.png" width="700"> | 


The [Poisson Multi-Bernoulli Mixture (PMBM) filter] is a gold standard for multi-target tracking. It is a sophisticated variation of Multiple Hypothesis Tracking (MHT), where several competing association hypotheses are generated and maintained at each estimation cycle. This differs from tracking methods such as Joint Probabilistic Data Association (JPDA) where all the association hypotheses are combined after every estimation cycle. This makes the PMBM filter more robust, at the price of higher computational requirements. 

So far, variations of the PMBM filter exist for the standard model, and for extended object tracking, where several detections can originate from each target. 

## Scope

During this assignment, the candidate will develop variations of the PMBM filter that can handle other violations of the standard model, such as ship wakes. 

## Proposed Tasks for the 5th year project

In the specialization project the goal is to make a JIPDA that can account for wake clutter. This problem has been addressed in a single-target context in Brekke2012 and Vo2009, and in JPDA context in Rødningsby2009. 

* Summarize similarities and differences between Brekke2012, Vo2009 and Rødningsby2009.
* Make a simple simulation environment to study targets with and without wakes.
* Specify a complete model for multi-target tracking with wakes and existence uncertainty. Pay particular attention to how the cardinalities of bona-fide clutter measurements and wake measurements are modeled.
* Revise an existing JIPDA implementation to work in accordance with the new models.
* Run experiments on both simulated data and real data (radar or lidar). Is the accuracy acceptable? Is the track-loss rate acceptable? Is the algorithm capable of fast initiation of new tracks?
* Write report.

## Proposed Tasks for the master thesis

In the master thesis the goal is to make a PMBM filter that can account for wake clutter. If time permits, the candidate may also include other non-standard elements such as targets spawning other targets, merged measurements or extended objects. In principle, the same modeling framework that was used in the specialization project can also be used here, but care must be exercised since the PMBM filter is more complex than the JIPDA.

* Consider whether any adjustments or more fundamental changes should be made to the work in the specialization project to improve performance.
* The presence of a wake will lead to considerably more non-target measurements. This is likely to make hypothesis exploration and cluster management more challenging. How can this be handled? 
* Should wake targets be treated in a different way than regular targets? If so, the multiple models framework may be appropriate. 
* Implement a PMBM filter, based on an existing code base and the models developed. 
* Investigate performance of the wake-PMBM filter in simulations and on real radar/lidar data.
* Write report.

|<img src="{{site.url}}/assets/wilthilsyn.jpg" width="700"> | 
| Erik Wilthil during [Autosea] experiments in Trondheimsfjorden where radar tracking was used |

## Prerequisites

The candidate should have had the course [TTK4250 Sensor Fusion], or take it in parallell with the specialization project. Experience with sensor fusion from extracurricular activities will also be useful. 

## References
Williams, J. (2015). "[Marginal multi-Bernoulli filters: RFS derivation of MHT, JIPDA, and association-based member.][Williams2015]" IEEE Transactions on Aerospace and Electronic Systems, vol. 51, no. 3.

Habtemariam et al. (2014): “[Measurement levelAIS/radar fusion][Habtemariam2014]”, Signal Processing.

Liland (2017): “[AIS Aided Multi Hypothesis Tracker][Liland2017]”, Master’s thesis, NTNU.


## Contact

Supervisor: [Edmund Brekke].  


|<img src="{{site.url}}/assets/MS_Nidarholm.jpg" width="700"> | 
| Example application 1: The autonomous ferry [Milliampere] should be able to use AIS for warm track initiation on the Munkholmen ferry when it approaches under the bridge. |

|<img src="{{site.url}}/assets/droneit.png" width="570"> | 
| Example application 2: The same theory can be used for fusion of drone transponders with 3D airport surveillance radar. |

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Williams2015]: https://ieeexplore.ieee.org/document/7272821
[Habtemariam2014]: https://www.sciencedirect.com/science/article/pii/S0165168414003636
[Liland2017]: https://brage.bibsys.no/xmlui/bitstream/handle/11250/2452107/16477_FULLTEXT.pdf?sequence=1
[Autosea]: https://www.ntnu.edu/autosea
[Milliampere]: https://www.ntnu.edu/autoferry
[Fundamentals of Sensor Fusion]: https://folk.ntnu.no/edmundfo/msc2020-2021/sf2020c.pdf