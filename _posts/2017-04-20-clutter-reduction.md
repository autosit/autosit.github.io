---
layout: post
title: Clutter Reduction and Target Detection in Maritime Radars using Machine Learning
category: SF
---
## Background
The Autosea project in colloboration with [AMOS](http://ntnu.edu/amos) aims to build knowledge that enables autonomous collision avoidance for maritime surface vehicles. Target tracking is an important capability of autonomous vehicles moving in environments with traffic, as the autonomous vehicle needs to keep track of all other moving objects in its vicinity, and predict their future movement.  Target tracking entails processing of data from various exteroceptive sensors, such as radar, lidar or camera. 

Radar is a reliable and robust sensor, but suffers from noise or clutter from land, sea, rain and birds. This makes object detection and tracking challenging. To build autonomous ships, robust observations are essential to achieve good performance.

Constant False Alarm Rate (CFAR) is an algorithm used in radars to separate targets from a background of clutter and noise. Automatic Radar Plotting Aid (ARPA) is functionality built into most maritime radars to detect and track targets in a radar image.
Are these methods sufficient to provide robust object detection and tracking for an autonomous ship?

Computer vision is a field of extensive research, and the tasks of object localization and classification have recently achieved great progress using machine learning and deep learning. Region Proposal Convolutional Neural Networks (R-CNN) can be used to localize and classify object in images. Can this network be trained to predict target locations in radar images as well? AIS data (Automatic Identification System) contains information about target position and velocity and can be used to supervise such a model.

The tasks of denoising and modelling unknown probability distributions have recently achieved great progress using machine learning and deep learning. Can machine learning methods be used to model and reduce the clutter in radar images and make target identification and tracking easier? 


![Radar image and desired output]({{site.url}}/assets/radarksx.png)

## Scope
The goal of this project is to explore methods from the computer vision and machine learning fields to improve clutter reduction and target detection in radar images. The scope is to review existing methods but also look into whether new machine learning approaches can improve upon current methods. Machine learning methods might include subspace methods like PCA, but also deep learning methods like autoencoders, R-CNN and generative models like Generative Adversarial Autoencoders (GAN).

## Proposed Tasks for the 5th year project

* Conduct a literature study on current approaches to target detection in maritime radars.
* Identify weaknesses in current approaches with regard to autonomous operations.
* Collect radar data and received AIS from a vessel in operation.
* Prepare a diverse data set with different weather conditions, sea conditions and objects in the proximity.
* Train a CNN to predict target locations from radar images.
* Test the implementation on the data set.
* Compare, if possible, to other methods.
* Write report.

## Proposed Tasks for the master thesis

* In the master’s project the goal shall be to extend the developments of the 5th year project.
* Conduct a literature study on current approaches to clutter reduction in maritime radars.
* Look into recent machine learning research and evaluate if unsupervised machine learning methods could improve on current clutter reduction algorithms.
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

R. Vicen-Bueno, R. Carrasco-Álvarez, M. Rosa-Zurera, J.C. Nieto-Borge, M.P. Jarabo-Amores: “Artificial Neural Network-based Clutter Reduction Systems for Ship Size Estimation in Maritime Radars”

H. M. Finn, R. S. Johnson: “Adaptive detection mode with threshold control as a function of spatially sampled clutter level estimates“, RCA Review, vol. 29, pp. 414-463, 1968.

N.B. Gálvez,  J.E. Cousseau,  J.L. Pasciaroni, O.E. Agamennoni: “Improved Neural Network Based CFAR Detection for Non Homogeneous Background and Multiple Target Situations“

Budiman Putra AR, Dayat Kurniawan,  M. Tajul Miftahushudur: “Switching CA/OS CFAR using Neural Network for Radar Target Detection in Non-Homogeneous Environment”

I. Goodfellow: “NIPS 2016 Tutorial: Generative Adversarial Networks”

R. Girshick, J. Donahue, T. Darrell, and J. Malik: “Rich feature hierarchies for accurate object detection and semantic segmentation“

