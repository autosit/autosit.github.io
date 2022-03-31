---
layout: post
title: The PMBM filter 3 -  Beyond the standard model
category: SF
---
## Background

Methods for multi-target tracking in maritime and military applications are typically based on a common set of model assumptions, which can be called the standard model (page 137 in [Fundamentals of Sensor Fusion]). In particular, two aspects of the standard model are worth mentioning. First, it invokes the at-most-one assumptions, which says that maximally one measurement comes from each target, and that at most one target can be the source of any measurement. Second, it invokes several independence assumptions. Both false alarms and new targets are according to the standard model independent of the previously existing targets. 

There are, however, many real-world applications where these assumptions fail to hold. An example is ship wakes in maritime tracking. 

|<img src="{{site.url}}/assets/ais_slide.png" width="700"> | 


The [Poisson Multi-Bernoulli Mixture (PMBM) filter] is a gold standard for multi-target tracking. It is a sophisticated variation of Multiple Hypothesis Tracking (MHT), where the probabilities of all sufficiently plausible data association hypotheses are calculated. 
For each of the data association hypotheses in the prior distribution, there will be several new association hypotheses in the posterior distribution. This differs from tracking methods such as Joint Probabilistic Data Association (JPDA) where the data association hypotheses are combined after every estimation cycle in order to mitigate complexity. 


## Scope

During this assignment, the candidate will develop a multi-target tracking algorithm that fuses both radar data and AIS data within the PMBM framework. 

## Proposed Tasks for the 5th year project

In the specialization project the main focus will be on mastering the fundamental building blocks of PMBM and radar-AIS fusion. The following tasks are proposed for the specialization project: 

* Make yourself familiar with multi-target tracking, random finite sets, MHT and PMBM. 
* Design simple toy scenarios that will enable careful analysis of the expected benefits of radar-AIS fusion. 
* Revise the hypothesis structure of the PMBM filter so that its hypotheses not only are able to account for associations between measurements in consecutive radar scans, but also associations between these and AIS tracks. 
* Revise the expressions for the probabilities of the association hypotheses according to the revision of the hypothesis structure. 
* Revise the estimation of target kinematics according to the two data sources.
* Test the revisions in simulations. 
* Write report.

## Proposed Tasks for the master thesis

In the MSc thesis the work should move from toy scenarios to more comprehensive simulations and real data. It is also desirable to strengthen the theoretical foundations of the work using the tools of random finite set theory such as functional derivatives. The following topics are expected to be of central importance. 

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