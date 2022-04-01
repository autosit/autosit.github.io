---
layout: post
title: The PMBM filter 3 -  Beyond the standard model
category: SF
---
## Background

Methods for multi-target tracking in maritime and military applications are typically based on a common set of model assumptions, which can be called the standard model (page 137 in [Fundamentals of Sensor Fusion]). In particular, two aspects of the standard model are worth mentioning. First, it invokes the at-most-one assumptions, which says that maximally one measurement comes from each target, and that at most one target can be the source of any measurement. Second, it invokes several independence assumptions. Both false alarms and new targets are according to the standard model independent of the previously existing targets. 

There are, however, many real-world applications where these assumptions fail to hold. An example is ship wakes in maritime tracking. Measurements from the wake are of limited use in estimating the state of the boat, and are therefore discarded as clutter. But since the wake always is behind the boat, there is a dependency between the wake and the target state that violates the standard model. 

|<img src="{{site.url}}/assets/boatwakes.jpg" width="700"> | 
| Wake behind a motorboat as seen in optical camera, lidar and radar. |

## Scope

During this assignment, the goal is to arrive at a variation of the Poisson Multi-Bernoulli Mixture (PMBM) filter that can handle other violations of the standard model, such as ship wakes. 

## Proposed Tasks for the 5th year project


The wake problem has previously been addressed in a single-target context by [(Brekke et al. 2012)] and [(Vo et al. 2008)], and in the multi-target Joint Probabilistic Data Assocation (JPDA) by [(Rødningsby et al. 2009)]. A natural stepping stone will be to make solution to the wake problem in the Joint Integrated Probabilistic Data Asociation (JIPDA), which also involves an existence probability for each track. The following tasks are suggested:

* Summarize similarities and differences between [(Brekke et al. 2012)], [(Vo et al. 2008)] and [(Rødningsby et al. 2009)].
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

## Prerequisites

The candidate should have had the course [TTK4250 Sensor Fusion], or take it in parallell with the specialization project. Experience with sensor fusion from extracurricular activities will also be useful. 

## References
Williams, J. (2015). "[Marginal multi-Bernoulli filters: RFS derivation of MHT, JIPDA, and association-based member.]([Williams2015)]" IEEE Transactions on Aerospace and Electronic Systems, vol. 51, no. 3.

Brekke, E., Hallingstad, O. and Glattetre, J. (2012) "[Improved target tracking in the presence of wakes.][(Brekke et al. 2012)]" IEEE Transactions on Aerospace and Electronic Systems, vol. 48, no. 2.

Rødningsby, A., Bar-Shalom, Y., Hallingstad, O. and Glattetre, J. (2012) "[Multitarget multisensor tracking in the presence of wakes.][(Rødningsby et al. 2009)]" Journal of Advances in Information Fusion, vol. 4, no. 2.

Vo, B.-T., Vo, B.-N. and Cantoni, A. (2012) "[Bayesian filtering with random finite set observations.][(Vo et al. 2008)]" IEEE Transactions on Signal Processing, vol. 56, no. 4.


## Contact

Supervisor: [Edmund Brekke].  


|<img src="{{site.url}}/assets/MS_Nidarholm.jpg" width="700"> | 
| Example application 1: The autonomous ferry [Milliampere] should be able to use AIS for warm track initiation on the Munkholmen ferry when it approaches under the bridge. |

|<img src="{{site.url}}/assets/droneit.png" width="570"> | 
| Example application 2: The same theory can be used for fusion of drone transponders with 3D airport surveillance radar. |

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[(Williams 2015)]: https://ieeexplore.ieee.org/document/7272821
[Habtemariam2014]: https://www.sciencedirect.com/science/article/pii/S0165168414003636
[Liland2017]: https://brage.bibsys.no/xmlui/bitstream/handle/11250/2452107/16477_FULLTEXT.pdf?sequence=1
[Autosea]: https://www.ntnu.edu/autosea
[Milliampere]: https://www.ntnu.edu/autoferry
[Fundamentals of Sensor Fusion]: https://folk.ntnu.no/edmundfo/msc2020-2021/sf2020c.pdf
[(Brekke et al. 2012)]: https://ieeexplore.ieee.org/document/6178045
[(Rødningsby et al. 2009)]: https://confcats_isif.s3.amazonaws.com/web-files/journals/entries/JAIF_article_multitarget2.pdf
[(Vo et al. 2008)]: https://people.eng.unimelb.edu.au/bnvo/vo/VVC_RFSO_SIC07.pdf
[TTK4250 Sensor Fusion]: https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet