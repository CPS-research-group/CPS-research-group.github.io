---
layout: single
author_profile: false
title: "Model-in-the-Loop Framework for Intelligent Cyber Physical System"
sitemap: false
permalink: /digital_twin/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Staff"
    text: "Heejong Park (Postdoc)"
  - title: "Research Student"
    text: "Gao Chuanchao (MEngg)"
  - title: "Former Staff"
    text: "Zhiheng Xu (Postdoc)"
---


******

# Research Motivation

The era of Industry 4.0 brings increased connectivity among devices, predictability through a large volume of data, and an ability to accurately capture states of the manufacturing shop-floor. Digital twin is a realistic virtual representation of machines or any form of living or non-living physical things that can accurately monitor, predict and optimize their operations. Although digital twin has received considerable attention recently in various domains such as manufacturing and cloud computing, etc., there is a number of limitations in the existing works:

1. Lack of support for various modeling formalisms that integrate with online data for creating a scalable twin.
2. Many focus on the traditional off-line simulation of high-fidelity models.
3. Most architectures are missing the details on how digital twin models are composed with each other using a formal model of computation.

******

# Our Approach

To build an accurate view of the physical system via a digital twin, the software architecture should support the utilization of different modeling strategies for creating the twin, where each model specializes in certain application domains. Furthermore, it is essential to support a method to combine such heterogeneous models in a consistent manner and utilize gathered online data from a physical system to provide a holistic understanding of the physical system’s state.

### The Architecture

{::options parse_block_html="true" /}

<div>
![arch](/_pages/assets/digital_twin/images/architecture.jpg){:style="max-width: 40%"}{: .align-right}
Our digital twin architecture consists of three layers. Each layer has a number of facilities that help the higher-level layers to perform more concrete tasks.
1. __Factory Layer__ has a set of physical assets and devices that control the manufacturing process and forwards data to the level above via the cyber-physical interface.
2. __Twin Layer__ is a fundamental part of the architecture that consists of twin models, online data, and various services for realizing the digital twin's modes of operations: _control_, _monitoring_, and _simulation_. Examples of models that can be imported into our architecture are Functional Mock-up Units (FMUs), Petri-Net, Esterel, FSMs
3. __Application Layer__ interacts with the digital twin for different use-case scenarios such as throughput monitoring, predictive maintenance, scheduling optimization, etc.
</div>
{: .align-left}

### Globally Asynchronous Locally Synchronous Semantics for Digital Twin

<div>
![gals](/_pages/assets/digital_twin/images/gals.jpg){:style="max-width: 40%"}{: .align-right}
![ticks](/_pages/assets/digital_twin/images/ticks.jpg){:style="max-width: 40%"}{: .align-right}
Intuitively, plants and controllers in our digital twin are heterogeneous models following Globally Asynchronous Locally Synchronous (GALS) model of computation (MoC) on a top level. The main features of our GALS MoC are:
1. Execution of a digital twin model is based on a sequence of logical ticks. In addition, a tick has its corresponding value in the continuous time domain.
2. Local execution determinism based on the Synchronous Reactive (SR) semantics, which is a subset of GALS.
3. Global asynchrony and communication between models in different _clock-domains_ via First-In-First-Out (FIFO) buffers.
</div>
{: .align-left}

### Case Study 1: Fault Monitoring and Analysis for the Manufacturing System

<div>
![fm-arch](/_pages/assets/digital_twin/images/fm-arch.jpg){:style="max-width: 30%"}{: .align-right}
![fm-dia](/_pages/assets/digital_twin/images/fm-diagram.jpg){:style="max-width: 30%"}{: .align-right}

The role of the fault monitoring and analysis application is to find the root cause of abnormal activities in the physical system via the digital twin by utilizing both the online data and the models of the twin. Detection of two different types of faults is illustrated based on the workpiece inspection time

1. _A fault in the conveyor belt's actuator_. In this scenario, a fault is indicated by intermittent spikes in the instantaneous power spectrum of the induction motor due to the induced motor stator current from the unbalanced rotor
2. _A fault in the actuator of the two-link planar robot_. A control algorithm for the workpiece placement on the conveyor belt is disturbed by actuator fault in the robot manipulator. This results in the misalignment of workpieces that causes increase in delays in the inspection process. The actuator fault in this scenario gradually drifts the manipulator's joints from the actual torque reference set by the controller
</div>
{: .align-left}
