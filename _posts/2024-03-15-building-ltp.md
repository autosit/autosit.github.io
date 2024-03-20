---
layout: post
title: Building marine traffic prediction models
category: LTP
---
## Background

Collision avoidance systems for autonomous vehicles depend on their ability to predict the future motion of other vehicles. For long-term prediction (LTP), simple kinematic models such as the constant velocity model will not be sufficient. Instead, the prediction model must utilize historical data or constraints, such as the fact that a car is unlikely to drive off the road or that a ship most likely will avoid grounding. 

Several approaches to LTP have been studied in the literature. These include both model-based approach, machine learning approaches, and hybrid approaches where a flexible model is learned from large amounts of data. However, there is a lack of comparisons between the different approaches. Furthermore, there is a need to study how different kinds of training data can be used. For example, many methods have been trained on data from the Automatic Identification System (AIS), while it also may be necessary to include radar data in order to get a full picture of the traffic patterns. 

|<img src="{{site.url}}/assets/predictionproblem.png" width="670"> | 
| The fundamental problem of long-term prediction: Standard kinematic models yield very large uncertainties after a couple of minutes. One must guess the other vessel's intentions if more accurate predictions are desired. | 

## Scope

The goal of this project is to compare different methods for long-term prediction, and to develop the pipeline needed to make on or more of these methods applicable to utilization in real-world autonomy. 
To strengthen the relevance to maritime surface autonomy, this pipeline should involve training on radar data recorded in Trondheimsfjorden or Trondheim Harbor. In other words, the goal is to build a long-term prediction model based on output from a radar tracking system. 

|<img src="{{site.url}}/assets/canaltracks.png" width="700"> | 
| Radar tracks from a data set of 1027 scenarios in the Trondheim City Canal. | 


## Proposed Tasks for the 5th year project

The goals of the specialization project is to make yourself familiar with the field of long-term prediction, and to bring radar tracking output into the picture. 

* Study and summarize different potential long-term prediction techniques, including conventional kinematic models, mean-reverting processes, bridging distributions, long-term short term memory, transformers, the modified neighbor course distribution method of [Dalsnes2016], etc. 
* Choose two or more of these methods to be trained on radar data. 
* Test the trained methods using relevant ship trajectories, and analyze performance
* Write report. 

## Proposed Tasks for the master thesis

The goal of the master thesis is to add additional features in order to make the prediction model more reliable and efficient. 
Such features could be:

* Utilization of class information. Should we expect the same behavior from Hurtigruta, a frigate and a fishing boat? 
* Utilization of online AIS information. If a ship tells us its destination or its course, can this be used to improve predictions?
* Taking potential collisions into account: Do we expect a ship to make evasive maneuvers because it is on a collision course? 

|<img src="{{site.url}}/assets/ais-data-trd.png" width="670"> | 
| Historical AIS data show many patterns for how ships tend to move. Understanding of these patterns can be used to plan trajectories so that dangerous situations are prevented from arising.  | 

## References
* Ahmad et al. (2016). "<a href="https://ieeexplore.ieee.org/document/7765149">Bayesian Intent Prediction in Object Tracking Using Bridging Distributions.</a>" IEEE Transactions on Cybernetics , vol. 48, no. 1. [Ahmad2016]  
* Hexeberg, S. (2017). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2452108">AIS-based Vessel Trajectory Prediction for ASV Collision Avoidance.</a>" MSc thesis, NTNU. [Hexeberg2017]  
* Dalsnes, B. (2018). "<a href="https://brage.bibsys.no/xmlui/handle/11250/2557943">Long-term Vessel Prediction Using AIS Data.</a>" MSc thesis, NTNU. [Dalsnes2018]

## Contact

Supervisor: [Edmund Brekke](www.ntnu.edu/employees/edmund.brekke) 