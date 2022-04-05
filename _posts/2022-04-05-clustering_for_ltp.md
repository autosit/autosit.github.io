---
layout: post
title: Unsupervised clustering of historical AIS dataset for long term trajectory prediction
category: LTP
---
## Background


A core requirement for collision avoidance systems for autonomous ships are the ability to predict the trajectories of the neighboring target ships over a longer time horizon. Model based predictions generally use linear models that are insufficient to make such predictions, particularly in the maneuvering scenarios. Consequently, data driven methods such as [Single Point Neighbor Search] (SPNS),  [Neighbor Course Distribition Method] (NCDM), [Gaussian Process] (GP) methods  and [Particle Filter] methods are developed to utilize the availablity of historical AIS dataset to aid the predictions. 


However, these methods do not exploit the inherent structure in the dataset represented by marine traffic lanes. Therefore, an unsupervised clustering method (Praveen Jain et al. 2022) based on Mean Shift algorithm, Agglomerative Heirarchical Clustering algorithm couple with Longest Common Subsequence trajectory similarity measure was developed to cluster the trajectories in the AIS dataset. The clustered dataset were used to make multi-modal probabilistic predictions using the NCDM and PF methods (See Figure 1 and 2 ) 

|<img src="{{site.url}}/assets/clustering.png" width="700"> | 
| Figure 1: The unsupervised clustering framework  |

|<img src="{{site.url}}/assets/ltp.png" width="700"> | 
| Figure 2: Representative result of long term prediction using the clustered dataset using time horizon of 40 minutes |
 

## Scope

During this assignment, the goal is to extend the preliminary results on clustering to incorporate larger areas of the marine environment in order to make them usable for long term prediction methods. In addition, the work could steer towards development of long term prediction algorithms that uses the clustered dataset building off on the existing work on Gaussian Processes or Particle Filters. 

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


## Autosit

The candidate will be associated with the AUTOSIT project, 
which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics.
The goal of the AUTOSIT project is 
to deliver algorithms for situational awareness that enable autonomous surface vessels (ASVs) to guess and predict the intentions of other vessels. 
The AUTOSIT project is a direct successor of the [AUTOSEA] project, which focused on [sensor fusion and collision avoidance for ASVs]. 
A list of students who previous have written master theses on autonomous ship technology at NTNU can be found [here].


## Contact

Supervisor: [Edmund Brekke].  


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
[here]: https://folk.ntnu.no/edmundfo/autoseastudents/autoseastudents.html
[AUTOSEA]: https://www.ntnu.edu/autosea/
[sensor fusion and collision avoidance for ASVs]: https://www.youtube.com/watch?v=XqZ_lbwwspo
