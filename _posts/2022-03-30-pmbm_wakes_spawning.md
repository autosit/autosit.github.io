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
* Design simple toy scenarios that will enable careful analysis of the expected benefits of radar-AIS fusion. 
* Revise the hypothesis structure of the PMBM filter so that its hypotheses not only are able to account for associations between measurements in consecutive radar scans, but also associations between these and AIS tracks. 
* Revise the expressions for the probabilities of the association hypotheses according to the revision of the hypothesis structure. 
* Revise the estimation of target kinematics according to the two data sources.
* Test the revisions in simulations. 
* Write report.

## Proposed Tasks for the master thesis

In the master thesis the goal is to make a PMBM filter that can account for wake clutter. If time permits, the candidate may also include other non-standard elements such as targets spawning other targets, merged measurements or extended objects. 

* Study mixture reduction techniques to limit the number of hypotheses. 
* Benchmark against other approaches to AIS-radar fusion, such as Liland (2017) or Habtemariam (2014).
* Generate more elaborate simulations and/or participate in field experiments to record real data. 

This project can be expanded into a PhD or integrated PhD for a candidate with sufficient skills, background knowledge and motivation. 

|<img src="{{site.url}}/assets/giorgio-den-helder.jpeg" width="700"> | 
| Giorgio Kufoalor during [Autosea] experiments in the Netherlands where AIS data were used |

|<img src="{{site.url}}/assets/wilthilsyn.jpg" width="700"> | 
| Erik Wilthil during [Autosea] experiments in Trondheimsfjorden where radar tracking was used |

## Prerequisites
This is a challenging project that goes to the core of modern theory in sensor fusion. The following recommendations should therefore be considered. 

- Experience with sensor fusion or radar systems from internships or voluntary activities will be useful.
- It will be very useful to have had significant exposure to statistics and estimation from courses beyond ITK, e.g., from IES or IMF at NTNU, or from exchange studies. 
- It will be useful to take the course TTK4250 Sensor Fusion in parallell with the specialization project, instead of the conventional 2.75 SP modules. 
- The candidate must like mathematics and to analyze problems on a very detailed level.

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