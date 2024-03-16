---
layout: post
title: A soft learning approach to extended object tracking
category: SF
---


## Background

Collision avoidance and situational awareness for autonomous surface vessels depend on methods for detection and tracking to know where other vehicles are and where they are heading. Vessels in confined waters such as canals and harbors often need to pass each other with small margins of error. This poses requirements to the tracking system, which only can be fulfilled by extended object tracking (EOT) utilizing the high resolution of modern sensors such as lidars, cameras or high-frequency radar. 

EOT is more complicated than point-based tracking because the algorithm must estimate the extent, or shape, of other vessels, in addition to their kinematic states. Thus, any EOT method must utilize some kind of representation of the extent. Representations such as random matrices, fixed shapes, Gaussian processes or Fourier expansions all have shortcomings. Ships come in all kinds of shapes and sizes, and it is difficult to specify a model that both is sufficiently flexible, computationally efficient and which achieves the ideal precision. 

As a solution to this, we have recently proposed a model where the ship perimeter is expressed by means of principal component analysis (PCA) over a large set of CAD models, which include many different shapes of relevance. This approach can be thought of as a form of soft classification or machine learning, where a fundamental form of the model is given, and the parameters are learned partly from offline training data, and partly from online sensor data. A major benefit with this approach is that is able to represent a wide range of ship shapes with a low number of parameters.  


## Scope

The goal of this project is to contribute to the development of a complete EOT method that uses this kind of representation that is learned from offline candidate shapes. You will be working closely with a PhD candidate who developed this representation. 


| <img src="{{site.url}}/assets/munkholmdeparting.png" width="370"> | | <img src="{{site.url}}/assets/lidar-and-camera.jpg" width="370"> |
|:---:| :---: |:---:|
| The Munkholmen tourist ferry as seen by a lidar (different colors are data from different time steps). | | The experimental setup where the lidar were recorded. It is evident that the boats in the background will cover several degrees in the field of view.|

## Proposed tasks for the specialization project

During the specialization project, you will be working closely with a PhD candidate who developed this representation. 
The specialization project will pursue answers to research questions such as the following:

* How is it best to do state estimation using this model? Is it preferable with a filtering approach or a smoothing approach?
* How can data association be done using this model? To which extent can feature information (colors, signal strength) aid the data association?
* For which sensors is this approach suitable? Much of the motivation stems for research lidar tracking. The model is also relevant for stereo cameras, which also can provide a similar point cloud, although with lower accuracy. A 2-dimensional version may also be relevant to high-resolution radar. 


## Proposed tasks for the MSc thesis 

The MSc thesis will continue in the same direction as the specialization project, or address research questions that were left for the future during the work with the specialization project. The following topics are likely to be of relevance:

* Multi-sensor fusion, using e.g. cameras and radar. 
* Integration with established tracking systems using variations of probabilistic data association or multiple hypothesis tracking. 
* Computational efficiency, to enable closed-loop testing. 

## Prerequisites
This is a list of *recommended* prerequisites for this master project.

- Strong programming skills in either Matlab, Python or C++. 
- You should have had the course [TTK4250 Sensor Fusion], or take it in parallel with the specialization project. Background in computer vision will also be useful. 


## Contact 
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo).

## Relevant literature

* Ruud, K., Brekke, E., & Eidsvik, J. (2018): “[LIDAR Extended Object Tracking of a Maritime Vessel Using an Ellipsoidal Contour Model](https://www.researchgate.net/publication/328890666_LIDAR_Extended_Object_Tracking_of_a_Maritime_Vessel_Using_an_Ellipsoidal_Contour_Model)”, SDF 2018.
* Granström, K., Reuter, S., Meissner, D. & Scheel, A. (2014): “[A multiple model PHD approach to tracking of cars under an assumed rectangular shape](https://ieeexplore.ieee.org/document/6915991/)”, FUSION 2014.
* Granström, K., Baum, M. & Reuter, S. (2016): “[Extended Object Tracking: Introduction, Overview and Applications](https://arxiv.org/abs/1604.00970)”, Journal of Advances in Information Fusion.
* Schuster, M. & Reuter, J. (2015): “[Target tracking in marine environment using automotive radar and laser range sensor](https://ieeexplore.ieee.org/document/7284009/)”, MMAR 2015.


See also some of the media coverage that the autonomous ferry project has received:

- <a href="https://www.tu.no/artikler/verdens-forste-forerlose-passasjerferge-kan-ga-over-en-kanal-i-trondheim/363790">https://www.tu.no/artikler/verdens-forste-forerlose-passasjerferge-kan-ga-over-en-kanal-i-trondheim/363790</a>
- <a href="https://trondheim24.no/nyheter/forerlos-framtid-flotmann-baten/">https://trondheim24.no/nyheter/forerlos-framtid-flotmann-baten/</a>
- <a href="http://trondheimhavn.no/nyhet/norsk-skipsteknologi-pa-tysk-tv-1248.aspx">http://trondheimhavn.no/nyhet/norsk-skipsteknologi-pa-tysk-tv-1248.aspx</a>

