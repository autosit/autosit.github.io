---
layout: post
title: Unsupervised Object Detection in Video from Maritime Environments
category: SF
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. Target tracking is an important capability of autonomous vehicles moving in environments with traffic, as the autonomous vehicle needs to keep track of all other moving objects in its vicinity, and predict their future movement.  Target tracking entails processing of data from various exteroceptive sensors, such as radar, lidar or camera. 

Radar is a reliable and robust sensor, but to build autonomous ships, camera sensors can complement the radar by confirming the observations, but also by classifying objects in the vicinity of the vessel. The camera has some strength because it sees colours and can detect objects with low radar reflectivity. In the future, a camera vision system should be able to replace the captain’s vision from the bridge. 

Computer vision is a field of extensive research, and the tasks of object localization and classification have recently achieved great progress using machine learning and deep learning. Methods for classification depends on “supervised” learning, but localization, segmentation and background subtraction are related operations that can be performed with “unsupervised” methods. 

The advantage of “unsupervised” methods is that the data can be used directly without the need to manually segment or classify the videos.

## Scope
The goal of this project is to explore “unsupervised” methods from computer vision and machine learning fields to remove unwanted information from the video. This means that we want to keep information about objects that might infer with the operation of the vessel. 

![Saliency maps]({{site.url}}/assets/saliency.png)

There exists many related variants of this task including background subtraction, saliency detection and foreground segmentation. Many methods exist for solving such tasks, but are they sufficient to provide robust object detection for an autonomous ship? The scope is to explore existing methods but also look into whether new machine learning approaches can improve upon current methods. Machine learning methods might include subspace methods like PCA, but also deep learning methods like autoencoders and generative models.

## Proposed Tasks for the 5th year project

* Conduct a literature study on current approaches to unsupervised object detection in video. See references for a starting point.
* Identify weaknesses in current approaches with regard to autonomous operations.
* Collect video from a vessel in operation.
* Prepare a diverse data set with different weather conditions, sea conditions, light conditions, background and objects in the proximity.
* Choose a promising method to implement.
* Test the implementation on the data set.
* Compare, if possible, to other methods.
* Write report.

## Proposed Tasks for the master thesis

* In the master’s project the goal shall be to extend the developments of the 5th year project.
* Look into recent machine learning research and evaluate if machine learning methods could improve the results.
* Choose one or two promising methods and test them on the data set.
* Compare the results with standard  methods.
* Write report.

## Prerequisites
Required background knowledge:
Experience in Python.
Interest in machine learning.

Useful, but not required, background knowledge:
Courses in statistics, algorithms development and/or artificial intelligence.
Experience with machine learning and deep learning.


## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo)
Co-supervisor: Arild Nøkland (Kongsberg Seatex)

## References

D. Prasad, D. Rajan, L. Rachmawati, E. Rajabally, C. Quek: “Video Processing from Electro-optical Sensors for Object Detection and Tracking in Maritime Environment: A Survey”

D. Prasad,C. Prasath, D. Rajan, L. Rachmawati, E. Rajabally, C. Quek: “Challenges in video based object detection in maritime scenario using computer vision”

