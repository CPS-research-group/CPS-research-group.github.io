---
layout: single
author_profile: false
title: "Resilient Cyber-Infrastructure for Manufacturing"
header:
  image: /assets/graphics/mainBanner.png
  video:
    id: 78mwXSsyYlw
    provider: youtube
sitemap: false
permalink: /resilience_cps/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Staff"
    text: "Sidharta Andalam (RF) \n \n Mohammad Shihabul Haque (RF) \n \n Daniel Ng Jun Xian (RA)"
  - title: "Research Students"
    text: "Ankita Sammadar (PhD) \n \n Daniel Ng Jun Xian (MEngg)"
---

******

# Research Motivation

Industry 4.0 has the potential to radically improve the productivity of manufacturing systems. The next generation of smart factories can perform more efficiently, collectively and resiliently. Existing resiliency techniques for the cyber-infrastructure of smart factories are inefficient due to two key limitations: 
1. They do not consider cross-layer (link, network and application) interactions. 
2. The techniques are centralised where all the decision making is mostly done at the highest-level.

******

# Our Approach

To enable a resilient cyber-infrastructure for Industry 4.0, we have presented a new contract-based methodology called CLAIR. Applications are described as a set of modular components that are distributed over a network. Contracts are used for describing the component’s interaction with other components (within and across layers). Finally, the contracts are monitored using runtime observers. We detect failures (contract violation) and react (change of contracts) to the disturbances, providing resiliency. Finally, using an industrial case study we validate the proposed architecture.

### 1. Proposed resilient cyber-infrastructure

![image-left](/_pages/assets/resilience_cps/images/CILayers.jpg){:height="50%" width="50%"}{: .align-right}
We believe that the proposed 3-layered cyber infrastructure with cross-layer communication is the first approach that tightly couples resiliency with the self-awareness attribute of Industry 4.0. The physical layer comprises physical components such as sensors, actuators, controllers and communication hardware. The platform layer embodies computational and communicational platforms such as operating systems and network managers. The application layer accommodates software components which describe the behavior of an application. E.g., product sorting on an assembly line.
{: .align-left}

### 2. Overview of components & contracts

![image-left](/_pages/assets/resilience_cps/images/ComponentOverview.jpg){:height="40%" width="40%"}{: .align-right}
**Interface:** Defines the I/O data channels of a component. Data is consumed from the interface, processed by the component and data output is produced at the interface. Each component has only one interface.  
**Behaviors:** It is possible to describe multiple behaviors of the component. Each behavior is associated with a Quality-of-Service. At runtime, the resilience manager selects a behavior for the component.  
**Contracts:** A contract specifies assumptions on the behavior of the environment and guarantees about the behavior of the component. At runtime, the resilience manager can switch between behaviors to react to disturbances in the system.  
**Resilience manager:** Detects faults (using observers) and decides (resilience logic) how best to react (response strategy).  
{: .align-left}

### 3. Observers for monitoring contracts
![image-left](/_pages/assets/resilience_cps/images/ObserversOverview.jpg){:height="40%" width="40%"}{: .align-right}
Static verification techniques are not generally adequate to validate whether a system meets the requirements (contracts satisfication). This may be because some of the requirements can only be validated with the data available at runtime (e.g. a sensor producing invalid data). As an alternative, system requirements can be monitored at runtime using observers. In our approach, observers are expressed using computational models such as finite state machines, timed automata or hybrid automata.  
{: .align-left}

******

# Evaluation testbed & demonstration

{% include video id="78mwXSsyYlw" provider="youtube" %}
> Video Caption: Assembly line setup for color-based sorting of work pieces. When the deadline for processing the color sensor data is not met, the following actions are expected.  
(1) If the fault can be handled internally, expected recovery time is informed to other components.  
(2) At the component-level, it can switch to a different behavior (less computation time). E.g., a different signal processing algorithm.  
(3) At the system-level, it is possible to reduce the speed of the motor, allowing more time for the processing of sensor data.  

******

# References
<ol>
<li>S. Andalam, D. J. X. Ng,A. Easwaran, K. Thangamariappan "Contract-based Methodology for Developing Resilient Cyber-Infrastructure in the Industry 4.0 Era", IEEE Embedded Systems Letters (under review).</li>
<li>S. Andalam, D. J. X. Ng,A. Easwaran, K. Thangamariappan "CLAIR: A Contract-based Framework for Developing
Resilient CPS Architectures", ACM Transactions on Cyber-Physical Systems (TCPS) (under review).</li>
</ol>