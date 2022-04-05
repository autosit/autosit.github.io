---
layout: post
title: Unsupervised clustering of historical AIS dataset for long term trajectory prediction
category: LTP
---
## Background


A core requirement for collision avoidance systems for autonomous ships are the ability to predict the trajectories of the neighboring target ships over a longer time horizon. Model based predictions generally use linear models that are insufficient to make such predictions, particularly in the maneuvering scenarios. Consequently, data driven methods such as Single Point Neighbor Search (SPNS) [(Hexeberg et al. 2017)],  Neighbor Course Distribition Method (NCDM) [(Dalsnes et al. 2018)], Gaussian Process (GP) methods [(Håvard, 2021)] and Particle Filter (Praveen Jain et al. 2022b) methods are developed to utilize the availablity of historical AIS dataset to aid the predictions. 


However, these methods do not exploit the inherent structure in the dataset represented by marine traffic lanes. Therefore, an unsupervised clustering method (Praveen Jain et al. 2022a) based on Mean Shift algorithm, Agglomerative Heirarchical Clustering algorithm couple with Longest Common Subsequence trajectory similarity measure was developed to cluster the trajectories in the AIS dataset. The clustered dataset were used to make multi-modal probabilistic predictions using the NCDM and PF methods (See Figure 1 and 2 ) 

|<img src="{{site.url}}/assets/clustering.png" width="700"> | 
| Figure 1: The unsupervised clustering framework  |

|<img src="{{site.url}}/assets/ltp.png" width="700"> | 
| Figure 2: Representative result of long term prediction using the clustered dataset using time horizon of 40 minutes |
 

## Scope

During this assignment, the goal is to extend the preliminary results on clustering to incorporate larger areas of the marine environment in order to make them usable for long term prediction methods. In addition, the work could steer towards development of long term prediction algorithms that uses the clustered dataset building off on the existing work on Gaussian Processes or Particle Filters. 

## Proposed Tasks for the 5th year project

The structure in the dataset, such as stop points, ports, etc can be exploited to further cluster the trajectories efficiently. To this end, the objectives for the 5th year project can be stated as follows:

* Review of relevant clutering methods, starting points are the publications [(Pallotta et al. 2013)] and (Praveen Jain et al. 2022a).
* Review of long term prediction methods, starting points are the publications [(Håvard, 2021)] and (Praveen Jain et al. 2022b).
* Explore the use of ports information to cluster dataset over a larger marine area.
* Formulation of a framework for efficient clustering of the dataset.
* Set up simulation environment for clustering and long term prediction using Python. Preliminary python scripts wil be made available to the candidate.
* Documentation of the findings.


## Proposed tasks for master thesis

The results of clustering can be used in the master thesis for developing long term trajectory prediction methods. To this end,

* Gaussian process methods can further be explored and its utility towards collision avoidance can be investigated.
* How can the clustered dataset over larger marine areas be exploited to make predictions for presence of multiple targets?
* Investigate the impact of prediction methods on the collision avoidance methods [(Johansen et al. 2016)]. Support with the control algorithm for collision avoidance will be provided to the candidate.
* Extensive simulation results and documentation.


## References

(Hexeberg et al. 2017), Hexeberg, S., Flåten, A. L., & Brekke, E. F. (2017, July). "[AIS-based vessel trajectory prediction][(Hexeberg et al. 2017)]". In 2017 20th International Conference on Information Fusion (Fusion) (pp. 1-8). IEEE.

(Dalsnes et al. 2018) B. R. Dalsnes, S. Hexeberg, A. L. Flåten, B. -O. H. Eriksen and E. F. Brekke, "[The Neighbor Course Distribution Method with Gaussian Mixture Models for AIS-Based Vessel Trajectory Prediction][(Dalsnes et al. 2018)]" 21st International Conference on Information Fusion (FUSION), 2018.

(Håvard, 2021) Håvard Skåra Mellbye, "[Gaussian Processes for long-term trajectory prediction using historical AIS data][(Håvard, 2021)]", Masters thesis, NTNU, 2021.

(Praveen Jain et al. 2022a) Praveen Jain, Edmund Brekke, Adil Rasheed, "Unsupervised Clustering of Marine Vessel Trajectories in Historical AIS Database", under review, International Conference of Information Fusion, 2022.

(Praveen Jain et al. 2022b) Praveen Jain, Edmund Brekke, Adil Rasheed, "Particle Filter methods for Vessel Trajectory Prediction using Historical AIS Data", under preparation.

(Pallotta et al. 2013), Pallotta, G., Vespe, M., & Bryan, K. (2013). "[Vessel pattern knowledge discovery from AIS data: A framework for anomaly detection and route prediction][(Pallotta et al. 2013)]". Entropy, 15(6), 2218-2245.

(Johansen et al. 2016) T. A. Johansen, T. Perez and A. Cristofaro, "[Ship Collision Avoidance and COLREGS Compliance Using Simulation-Based Control Behavior Selection With Predictive Hazard Assessment][(Johansen et al. 2016)]," in IEEE Transactions on Intelligent Transportation Systems, 2016.



## Prerequisites

The candidate should have had the course [TTK4250 Sensor Fusion], or take it in parallell with the specialization project. Experience with sensor fusion from extracurricular activities will also be useful. 


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

[(Hexeberg et al. 2017)]: https://ieeexplore.ieee.org/abstract/document/8009762
[(Dalsnes et al. 2018)]: https://ieeexplore.ieee.org/abstract/document/8455607
[(Håvard, 2021)]: https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2831564
[(Pallotta et al. 2013)]: https://www.mdpi.com/1099-4300/15/6/2218
[(Johansen et al. 2016)]: https://ieeexplore.ieee.org/document/7464354

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
