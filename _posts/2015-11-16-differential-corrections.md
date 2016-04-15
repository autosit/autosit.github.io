---
layout: post
title: Accurate navigation with CPOS
subtitle: Differential corrections for low-cost INS
category: SF
---
## Background
Conventional low-cost GPS solutions typically obtain an accuracy of 2-3 meters. More accurate position estimates can be obtained by differential corrections. The traditional method of suppling these corrections are from a user base station with real-time kinematics (RTK) corrections. The corrections are typically transmitted from the base station to the moving vehicle on a radio link.

An alternative method for centimeter-level accuracy is the [CPOS](http://kartverket.no/Posisjonstjenester/CPOS) service from Kartverket. This service communicates with Kartverket through GSM or an internet connection, and sets up a virtual reference station close to the vehicle. This means that the base station can be avoided by equipping the vehicle with an internet modem.

Low-cost inertial measurement units (IMUs) are typically used in smartphones and consumer-level quadcopters. However, they have considerable error characteristics, which are usually corrected with GPS measurements. The measurements are also used to estimate the IMU errors.

## Scope
The task is to determine to what extent these low-cost sensors benefits from accurate GPS measurements. The main challenge is that the measurements can be applied to the sensor error estimates instead of the position estimate. It is also desirable to compare different types of navigation methods.

## Proposed Tasks
1. Perform a litterature review over INS/GPS navigation techniques, and the differences in RTK and differential corrections such as CPOS.
3. Compare the effect of differential corrections in INS/GPS systems. There are several relevant comparisons that can be made:
    * The quality of the IMU. High-quality IMU data may be available via a [Kongsberg Seapath](http://www.km.kongsberg.com/ks/web/nokbg0240.nsf/AllWeb/723E6C71BD3A17A6C1256B82002D5616) system.
    * The navigation algorithm. There exists several algorithms such as Kalman filters and nonlinear observers which might have different results in this context.
4. Present the results and discuss limitations and challenges.

## Prerequisites
* [TTK4115](http://www.ntnu.edu/studies/courses/TTK4115) - Linear System Theory

The following topics should be taken concurrently to the project thesis:
* [TTK4190](http://www.ntnu.edu/studies/courses/TTK4190) - Guidance and Control of Vehicles
* [TTK5](http://www.itk.ntnu.no/emner/fordypning/TTK5) - Kalman Filtering and Navigation

## Autosea
The candidate will be associated with the AUTOSEA project, which is a collaborative research project between NTNU, DNV GL, Kongsberg Maritime and Maritime Robotics, focused on achieving world-leading competence and knowledge in the design and verification of methods and systems for sensor fusion and COLAV for ASVs. The project has access to supervision and physical test platforms through our industry partners.

## Contact 
For more information, contact main supervisor [Edmund F. Brekke](http://www.ntnu.no/ansatte/edmundfo).
