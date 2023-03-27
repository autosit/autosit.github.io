---
layout: post
title: Multiple hypothesis tracking with mixture reduction
category: SF
---
## Background


The [Poisson Multi-Bernoulli Mixture (PMBM) filter] is a gold standard for multi-target tracking. It is a sophisticated variation of Multiple Hypothesis Tracking (MHT), where the probabilities of all sufficiently plausible data association hypotheses are calculated. 
An alternative is the Joint Integrated Probabilistic Data Association (JIPDA). 
In this method, the association hypoteses are merged by means of mixture reduction, so that each target can be represented by a single Gaussian. 
This imposes significantly lower computational demands, and is therefore typically preferred in real-time systems. 

For single-target tracking, compromises between these two philosophies have been explored. 
One could for instance design the tracking method so that the posterior probability distribution of the target consists of maximally 5 Gaussians. 
In multi-target tracking it is not straightforward to do similar things, because different targets are present in different hypotheses, and the overall knowledge about the targets must be represented by something more complex than a conventional probability density function, such as a random finite set density. 

Yet another approach to multi-target tracking is found in the Probability Hypothesis Density (PHD) filter, where the knowledge about the targets is approximated by a Poisson point process (PPP). Related to this is the idea of recycling: To take low-quality tracks out of the association hypotheses (i.e. the MBM component of the PMBM filter) and insert them into a PPP (i.e. the P component of the PMBM filter) or a separate dummy hypothesis. 

In a [currently ongoing MSc project], we are studying how marginal track probabilities can be calculated for the PMBM filter by means of loopy belief propagation (LBP), in order to support recycling. The proposed project is intended to build upon this work. 



## Scope

The long-term goal of this project is to develop a tracking method which can be tuned so that it behaves like a PMBM filter, JIPDA or PHD filter to arbitrary degrees. This could enable real-time systems to utilise the full power of PMBM when it is possible, for limited parts of the problem where it is deemed advisable, while reducing to JIPDA or PHD filter for other parts of the problem where this is believed to be sufficient. 

|<img src="{{site.url}}/assets/mhthypos.png" width="700"> | 
| The top 5 hypotheses, out of 602, for a simple tracking scenario. Can we combine the hypotheses into a smaller collection with essentially the same information? |


## Proposed Tasks for the 5th year project

* Make yourself familiar with multi-target tracking, random finite sets, mixture reduction and graphical models.
* Conduct a literature study on existing techniques for mixture reduction of Gaussians, Bernoulli merging and moment-based approximations of random finite sets. Perform simulations to investigate the behaviour of some of the approaches. 
* Consider then the case of a JIPDA for simple scenarios: Can you use mixture reduction to produce two or three merged hypotheses instead of a single merged hypothesis?
* Implement, simulate and compare performance with standard JIPDA and full-scale PMBM. 
* Write report.

## Proposed Tasks for the master thesis

In the MSc thesis the focus should be on generalizing the developments from the specialization project in order to achieve a flexible combination of PMBM, JIPDA and PHD. The following topics may play a central role:

* LBP or Bayes tree techniques for direct evaluation of marginal track probabilities. 
* Efficient generalizations of Murty's method for hypothesis exploration. 
* N-scan merging, [target labels] and [sets of trajectories].


## Prerequisites

This is a core [Sensor Fusion] project. 


## Autosit

The candidate will be associated with the [AUTOSIT] project, 
which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics.
The goal of the [AUTOSIT] project is 
to deliver algorithms for situational awareness that enable autonomous surface vessels (ASVs) to guess and predict the intentions of other vessels. 
The [AUTOSIT] project is a direct successor of the [AUTOSEA] project, which focused on [sensor fusion and collision avoidance for ASVs]. 
A list of students who previous have written master theses on autonomous ship technology at NTNU can be found [here].

## References
Williams, J. (2015). "[Marginal multi-Bernoulli filters: RFS derivation of MHT, JIPDA, and association-based member.][Williams2015]" IEEE Transactions on Aerospace and Electronic Systems, vol. 51, no. 3.

Salmond, D. J. (1990). "[Mixture reduction algorithms for target tracking in clutter.][Salmond1990]" Proceedings of SPIE.

Brekke, E. and Tokle, L.-C. (2022): “[Hypothesis Exploration in Multiple Hypothesis Tracking with Multiple Clusters](https://folk.ntnu.no/edmundfo/fusion2022preprints/BrekkeTokleExploration.pdf)”, Proceedings of FUSION. 

Fontana, M., Garcia-Fernandez, A. and Maskell, S. (2020): “[Bernoulli merging for the Poisson multi-Bernoulli mixture filter](https://ieeexplore.ieee.org/abstract/document/9190443)”, Proceedings of FUSION. 


## Contact

Supervisor: [Edmund Brekke].  

[AUTOSEA]: https://www.ntnu.edu/autosea/
[here]: https://folk.ntnu.no/edmundfo/autoseastudents/autoseastudents.html
[Edmund Brekke]: www.ntnu.edu/employees/edmund.brekke
[Williams2015]: https://ieeexplore.ieee.org/document/7272821
[Salmond1990]: https://www.spiedigitallibrary.org/conference-proceedings-of-spie/1305/0000/Mixture-reduction-algorithms-for-target-tracking-in-clutter/10.1117/12.2321784.full?SSO=1
[Liland2017]: https://brage.bibsys.no/xmlui/bitstream/handle/11250/2452107/16477_FULLTEXT.pdf?sequence=1
[AUTOSIT]: https://www.ntnu.edu/autosit
[AUTOFERRY]: https://www.ntnu.edu/autoferry
[(Garcia-Fernandez et al. 2018)]: https://ieeexplore.ieee.org/document/8289337
[(Brekke and Tokle 2022)]: https://folk.ntnu.no/edmundfo/fusion2022preprints/BrekkeTokleExploration.pdf
[Sensor Fusion]: https://www.ntnu.no/studier/emner/TTK4250#tab=omEmnet
[Poisson Multi-Bernoulli Mixture (PMBM) filter]: https://ieeexplore.ieee.org/document/7272821
[currently ongoing MSc project]: https://folk.ntnu.no/edmundfo/msc2023-2024/odin_fordypningsprosjekt.pdf
[target labels]: https://ba-ngu.vo-au.com/vo/VV_Conjugate_TSP13.pdf
[sets of trajectories]: https://ieeexplore.ieee.org/document/8731733