---
layout: single
author_profile: false
title: "Real-Time Scheduling of Deep Neural Network Workloads with Performance and Data Dependency"
sitemap: false
permalink: /coscheduling/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Staff/Students"
    text: "Chuanchao Gao (Research Associate)"
---

******

# Research Motivation
Cyber-physical systems (CPS) are a class of systems that combine both software tasks and physical sensors/actuators to interact with the physical world. Such systems are often responsible for control in safety-critical applications such as smart grids, autonomous vehicles, inspection drones, and intersection monitoring. In such applications, it is necessary that the CPS accurately processes sensor data and that it meets strict safety requirements, as a failure could lead to catastrophic consequences, including loss of human life. Safe operation requires two conditions to be satisfied:
1. The results of computations lead to *safe* control actions given the environment state.
2. Computations are time-bounded such that the applied control actions have their intended effect.
For example, in an autonomous vehicle, successfully detecting all pedestrians around the vehicle is necessary to avoid a fatal collision, but the detection also needs to take place by a critical deadline so that the system is capable of taking appropriate actions to avoid the collision.

![image-right](/_pages/assets/coscheduling/pipeline.png){:height="40%" width="40%"}{: .align-right}
![image-right](/_pages/assets/coscheduling/schedule.png){:height="40%" width="40%"}{: .align-right}

In modern CPS, deep neural networks (DNNs) are widely used for planning, perception, and control tasks. Prior research has led to DNNs that are capable of generalizing to new environments or performing tasks more accurately than non-DNN based models. However, end-to-end DNNs that take sensory input and determine a control action are not popular for safety-critical tasks such as those found in CPS. Instead, pipelines of models are used, some of which can be implemented as DNNs while others can be implemented using classical algorithms. These pipelines allow for greater explainability and a more modular architecture that enables simpler DNNs to be trained on specific tasks and replaced as necessary. The figure shows an example of such a pipeline in an autonomous vehicle. The pipeline is divided into planning, perception, and control stages, with *data dependencies* between the tasks. Additionally, given the result of one task, we may be able to predict the performance of another task; we call this a *performance dependency*. For example, if many vehicles are present, the performance of lane detection may suffer due to occlusion. This necessitates a scheduling plan that allocates more compute resources to the lane detection task to account for this challenging environment it faces. Thus, as one task makes predictions about the operating environment, the schedule of another performance dependent task may have to be dynamically adapted for efficiency purposes, while still meeting task deadlines. 
Thus, a comprehensive real-time (deadline aware) scheduling framework considering performance as well as data dependencies among different tasks of the pipeline is required. Note, these pipelines would typically be executed on resource-constrained hardware since most CPS deployments are embedded in nature, and hence optimized resource scheduling is essential for efficient system performance.
