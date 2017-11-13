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
  nav: resilience_cps_ppl
#  - title: "Research Staff"
#    text: "Sidharta Andalam (RF) \n \n Mohammad Shihabul Haque (RF) \n \n Daniel Ng Jun Xian (RA)"
#  - title: "Research Students"
#    text: "Ankita Sammadar (PhD) \n \n Daniel Ng Jun Xian (MEngg)"

component_observers:
  - image_path: /_pages/assets/resilience_cps/images/CILayers.jpg
    alt: "placeholder image 1"
    title: "1. Proposed cyber-infrastructure"
    excerpt: "We believe that the proposed 3-layered cyber infrastructure with cross-layer communication is the first approach that tightly couples resiliency with the self-awareness attribute of Industry 4.0. The physical layer comprises physical components such as sensors, actuators, controllers and communication hardware. The platform layer embodies computational and communicational platforms such as operating systems and network managers. The application layer accommodates the software components which describe the behavior of an application. E.g., product sorting on an assembly line."
    
  - image_path: /_pages/assets/resilience_cps/images/ComponentOverview.jpg
    alt: "placeholder image 2"
    title: "2. Overview of components & contracts"
    excerpt: "Interface: defines the I/O data channels of a component. Data is consumed through input interface, processed by the component, and output data is produced. Each component has only one interface. Behaviors: It is possible to describe multiple behaviors of the component. Each behavior is associated with a QoS. At runtime, the resilience manager select the behavior of the component. Contracts: A contract specifies assumptions on the behavior of the environment & guarantees about the behavior of the component. At runtime, the resilience manager can switch between contracts to react to the disturbances in the system. Resilience manager: Detect faults (using Observers) and decides (control logic) how best to react (response strategy)."
  - image_path: /_pages/assets/resilience_cps/images/ObserversOverview.jpg
    alt: "placeholder image 2"
    title: "3. Observers for monitoring contracts"
    excerpt: "Static verification techniques are not generally adequate to validate whether or not the system meets the requirements (satisfies the contracts). This may be because some of the requirements can only be decided with the data available at runtime (e.g., a sensor producing invalid data). As an alternative, system requirements can be monitored at runtime using observers. In our approach, observers are expressed using computational models such as finite state machine, timed automaton or hybrid automata."
  - image_path: /_pages/assets/resilience_cps/images/PerUtiVSTime.jpg
    alt: "placeholder image 2"
    title: "4. New metric for quantifying resiliency"
    excerpt: "Due to the heterogeneous nature of the CPS infrastructure a multi-dimensional metric is required to quantitatively assess the resiliency of the system. The challenge is to develop a sensible abstraction across layers, while respecting the richness of the cyber-infrastructure. We discuss the abstractions that enable us to reason about the performance and resiliency of a system. The abstract metric involves (1) Availability, (2) Demand, (3) Utilisation, (4) Performance, and (5) Resilience."
---

******

# Problem statement
Industry 4.0 has the potential to radically improve the productivity of manufacturing systems. The next generation of smart factories can perform more efficiently, collectively and resiliently. Existing resiliency techniques are inefficient due to two key limitations: (1) They do not consider cross-layer interactions. (2) The techniques are centralised where all the decision making is mostly done at the highest-level.

# Our approach

To enable a resilient cyber-infrastructure for Industry 4.0, we have presented a new contract-based methodology called CLAIR. Applications are described as a set of modular components that are distributed over a network. Contracts are used for describing the component’s interaction with other components (within and across layers). Finally, the contract are monitored using runtime observers. We detect failures (contract violation) and react (change of contracts) to the disturbances, providing resiliency. Finally, using an industrial case study we have validated the proposed architecture.

{% include feature_row id="component_observers" %}

# Evaluation testbed & demonstration
{% include video id="78mwXSsyYlw" provider="youtube" %}

> Video Caption: Assembly line setup for color-based sorting for work pieces. When the deadline for processing the Color Sensor data is not met, the following actions are expected. (1) Component communicates the occurrence of the fault with other components. (2) If the fault can be handled internally, the expected recovery time is informed to others. (3) At component-level, it can switch to a different contract (a behavior with less computation time). E.g., different signal processing algorithm. (4) At system-level, it is possible to reduce the speed of the motor, allowing more time for processing sensor data. All the decisions are guided by a new resilience metric

# References
<ol>
<li>S. Andalam, D. J. X. Ng,A. Easwaran, K. Thangamariappan "Contract-based Methodology for Developing Resilient Cyber-Infrastructure in the Industry 4.0 Era", IEEE Embedded Systems Letters (under review).</li>
<li>S. Andalam, D. J. X. Ng,A. Easwaran, K. Thangamariappan "CLAIR: A Contract-based Framework for Developing
Resilient CPS Architectures", ACM Transactions on Cyber-Physical Systems (TCPS) (under review).</li>
</ol>