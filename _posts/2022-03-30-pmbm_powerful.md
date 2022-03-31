---
layout: post
title: The PMBM filter 1 - The most powerful tracker in the world
category: SF
---
## Background


The Poisson Multi-Bernoulli Mixture (PMBM) filter is a gold standard for multi-target tracking. It is a sophisticated variation of Multiple Hypothesis Tracking (MHT), where the probabilities of all sufficiently plausible data association hypotheses are calculated. 
For each of the data association hypotheses in the prior distribution, there will be several new association hypotheses in the posterior distribution. This differs from tracking methods such as Joint Probabilistic Data Association (JPDA) where the data association hypotheses are combined after every estimation cycle in order to mitigate complexity. 

To make a PMBM filter run in real time, one has to use other heuristics and approximations. These including pruning and cluster management. 
The core principle in cluster management is to work with tracks that are far apart independently. Cluster management depends on procedures to merge clusters when the clusters get so close that they cannot be separated, and procedures to split clusters when a cluster safely can be decomposed into several independent tracking problems. 
Cluster management is important because multi-target tracking in reality reduces to single-target tracking 99&#37; of the time. The number of hypotheses needed to describe the posterior distribution in a single-target tracking problem will be much lower than the number of hypotheses needed in a tracking problem with several targets. 

A Matlab implementation of a PMBM filter without cluster management was recently reported in [(Garcia-Fernandez et al. 2018)].  Since then, a Matlab implementation of PMBM with cluster management has been made, which uses a novel algorithm for combined hypothesis search cluster merging [(Brekke and Tokle 2022)]. 




## Scope

The primary objective of this project is to implement a PMBM filter which can be used as part of the autonomy pipelines in maritime surface autonomy at NTNU. All of the algorithmic building blocks are ready, although there is certainly room for improvement. Core challenges are to implement the building blocks in a suitable language (possible a combination of Python and C), improve run-time and make sure the code is streamlined, transparent and configurable.  

## Proposed Tasks for the 5th year project

* Make yourself familiar with multi-target tracking, random finite sets, MHT and PMBM. 
* Design simple toy scenarios that will enable careful analysis of the expected benefits of radar-AIS fusion. 
* Revise the hypothesis structure of the PMBM filter so that its hypotheses not only are able to account for associations between measurements in consecutive radar scans, but also associations between these and AIS tracks. 
* Revise the expressions for the probabilities of the association hypotheses according to the revision of the hypothesis structure. 
* Revise the estimation of target kinematics according to the two data sources.
* Test the revisions in simulations. 
* Write report.

## Proposed Tasks for the master thesis

In the MSc thesis the focus should be on allowing the user to chose the right trade-off between run-time and performance. 

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

Garcia-Fernandez, A., Williams, J., Granström, K and Svensson, L. (2018). "[Poisson multi-Bernoulli mixture filter: direct derivation and implementation.][(Garcia-Fernandez et al. 2018)]" IEEE Transactions on Aerospace and Electronic Systems.

* Brekke, E. and Tokle, L.-C. (2022): “[Hypothesis Exploration in Multiple Hypothesis Tracking with Multiple Clusters](https://folk.ntnu.no/edmundfo/fusion2022preprints/BrekkeTokleExploration.pdf)”, Submitted to Fusion 2022. 


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
[(Garcia-Fernandez et al. 2018)]: https://ieeexplore.ieee.org/document/8289337
[(Brekke and Tokle 2022)]: https://folk.ntnu.no/edmundfo/fusion2022preprints/BrekkeTokleExploration.pdf