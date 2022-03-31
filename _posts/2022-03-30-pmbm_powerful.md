---
layout: post
title: The PMBM filter 1 - The world's most powerful tracker
category: SF
---
## Background


The [Poisson Multi-Bernoulli Mixture (PMBM) filter] is a gold standard for multi-target tracking. It is a sophisticated variation of Multiple Hypothesis Tracking (MHT), where the probabilities of all sufficiently plausible data association hypotheses are calculated. 
For each of the data association hypotheses in the prior distribution, there will be several new association hypotheses in the posterior distribution. This differs from tracking methods such as Joint Probabilistic Data Association (JPDA) where the data association hypotheses are combined after every estimation cycle in order to mitigate complexity. 

To make a PMBM filter run in real time, one has to use other heuristics and approximations. These including pruning and cluster management. 
The core principle in cluster management is to work with tracks that are far apart independently. Cluster management depends on procedures to merge clusters when the clusters get so close that they cannot be separated, and procedures to split clusters when a cluster safely can be decomposed into several independent tracking problems. 
Cluster management is important because multi-target tracking in reality reduces to single-target tracking 99&#37; of the time. The number of hypotheses needed to describe the posterior distribution in a single-target tracking problem will be much lower than the number of hypotheses needed in a tracking problem with several targets. 

A Matlab implementation of a PMBM filter without cluster management was recently reported in [(Garcia-Fernandez et al. 2018)].  Since then, a Matlab implementation of PMBM with cluster management has been made, which uses a novel algorithm for combined hypothesis search and cluster merging [(Brekke and Tokle 2022)]. 



## Scope

The primary objective of this project is to implement a PMBM filter which can be used as part of the autonomy pipelines in maritime surface autonomy at NTNU. All of the algorithmic building blocks are ready, although there is certainly room for improvement. Core challenges are to implement the building blocks in a suitable language (possible a combination of Python and C), improve run-time and make sure the code is streamlined, transparent and configurable.  

## Proposed Tasks for the 5th year project

* Make yourself familiar with multi-target tracking, random finite sets, MHT and PMBM. 
* Design the software architecture of an overall PMBM filter, taking the pipelines used in [Autoferry] og [Autosit] into account. 
* Identify bottlenecks, and open source code elements that can be used as part of the implementation. 
* Implement procedures for prediction, estimation, cluster merging, hypothesis generation, pruning and cluster merging.
* Verify the procedures and combine them in a complete PMBM filter.
* Write report.

## Proposed Tasks for the master thesis

In the MSc thesis the focus should be on allowing the user to chose the right trade-off between run-time and performance. The following tasks are meant to support this goal.

* Implement visualization tools for the PMBM filter. 
* Implement solutions to bottlenecks in C, C++ or similar.
* Develop additional heuristics to control the number of clusters, hypotheses etc. 
* Investigate whether it is possible to include a limited level of JPDA-style hypothesis merging. 
* Design benchmark scenarios, and compare with other state-of-the-art tracking methods.


## Prerequisites

The candidate should have had the course [TTK4250 Sensor Fusion]. Strong programming skills are essential.


## References
Williams, J. (2015). "[Marginal multi-Bernoulli filters: RFS derivation of MHT, JIPDA, and association-based member.][Williams2015]" IEEE Transactions on Aerospace and Electronic Systems, vol. 51, no. 3.

Garcia-Fernandez, A., Williams, J., Granström, K and Svensson, L. (2018). "[Poisson multi-Bernoulli mixture filter: direct derivation and implementation.][(Garcia-Fernandez et al. 2018)]" IEEE Transactions on Aerospace and Electronic Systems.

* Brekke, E. and Tokle, L.-C. (2022): “[Hypothesis Exploration in Multiple Hypothesis Tracking with Multiple Clusters](https://folk.ntnu.no/edmundfo/fusion2022preprints/BrekkeTokleExploration.pdf)”, Submitted to Fusion 2022. 


## Contact

Supervisor: [Edmund Brekke].  

[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Williams2015]: https://ieeexplore.ieee.org/document/7272821
[Habtemariam2014]: https://www.sciencedirect.com/science/article/pii/S0165168414003636
[Liland2017]: https://brage.bibsys.no/xmlui/bitstream/handle/11250/2452107/16477_FULLTEXT.pdf?sequence=1
[Autosit]: https://www.ntnu.edu/autosit
[Autoferry]: https://www.ntnu.edu/autoferry
[(Garcia-Fernandez et al. 2018)]: https://ieeexplore.ieee.org/document/8289337
[(Brekke and Tokle 2022)]: https://folk.ntnu.no/edmundfo/fusion2022preprints/BrekkeTokleExploration.pdf
[TTK4250 Sensor Fusion]: https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet
[Poisson Multi-Bernoulli Mixture (PMBM) filter]: https://ieeexplore.ieee.org/document/7272821