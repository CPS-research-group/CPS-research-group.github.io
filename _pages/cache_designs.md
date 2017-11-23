---
layout: single
author_profile: false
title: "Cache Design for Predictability"
header:
  image: /assets/graphics/mainBanner.png
  video:
    id: 78mwXSsyYlw
    provider: youtube
sitemap: false
permalink: /cache_designs/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Staff"
    text: "Sidharta Andalam (RF) \n \n Mohammad Shihabul Haque (RF) \n \n Daniel Ng Jun Xian (RA)"
  - title: "Research Students"
    text: "Ankita Sammadar (PhD) \n \n Daniel Ng Jun Xian (MEngg)"
    
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
To ensure timely completion of tasks, real-time systems perform schedulability analysis. This analysis takes the Worst-Case-Execution-Time (WCET) of each task as input. To estimate a task's WCET bound offline, predicted behaviour of each level in the processor cache memory hierarchy (i.e. a safe upper bound for the number of cache misses encountered by the task) is required. However, when muticore processors are used, behaviour of each level in the cache hierarchy becomes extremely challenging firstly because of the interdependency of concurrently running tasks, and secondly, because of sharing by multiple processing cores. To overcome this challenge, a wide body of research tried to design suitable prediction mechanism and cache architecture; however, failed to come up with a pragmatic and efficient solution.
******

# Our approach
We investigate and design cache management-based opportunities to overcome the cache predictability challenge for multicores. One direction of our curent approach is designing such cache replacement policies that (i) are easy-to-implement in conventional set-associative cache memories, (ii) enable private and/or shared cache behavior prediction using intuitive and simple mechanisms, (iii) make efficient utilization of cache space, and (iv) maintain minimal performance during fierce cache contention as well as during uneven cache utilization by the processing cores. Another direction is designing prefetching techniques and alterantive to prefetching thechniques that are suitable, efficient and pragmatic for multicore real-time systems.

### 1. Replacement Policy for Shared Cache
We believe that the proposed 3-layered cyber infrastructure with cross-layer communication is the first approach that tightly couples resiliency with the self-awareness attribute of Industry 4.0. The physical layer comprises physical components such as sensors, actuators, controllers and communication hardware. The platform layer embodies computational and communicational platforms such as operating systems and network managers. The application layer accommodates the software components which describe the behavior of an application. E.g., product sorting on an assembly line.

![image-left](/_pages/assets/cache_designs/images/Shared_Cache.jpg)

### 2. Proposed Replacement Policy for Private Cache
Interface: defines the I/O data channels of a component. Data is consumed through input interface, processed by the component, and output data is produced. Each component has only one interface. Behaviors: It is possible to describe multiple behaviors of the component. Each behavior is associated with a QoS. At runtime, the resilience manager select the behavior of the component. Contracts: A contract specifies assumptions on the behavior of the environment & guarantees about the behavior of the component. At runtime, the resilience manager can switch between contracts to react to the disturbances in the system. Resilience manager: Detect faults (using Observers) and decides (control logic) how best to react (response strategy).  

![image-left](/_pages/assets/cache_designs/images/Reconfigurable.jpg)

# References
<ol>
<li>S. Andalam, D. J. X. Ng,A. Easwaran, K. Thangamariappan "Contract-based Methodology for Developing Resilient Cyber-Infrastructure in the Industry 4.0 Era", IEEE Embedded Systems Letters (under review).</li>
<li>S. Andalam, D. J. X. Ng,A. Easwaran, K. Thangamariappan "CLAIR: A Contract-based Framework for Developing
Resilient CPS Architectures", ACM Transactions on Cyber-Physical Systems (TCPS) (under review).</li>
</ol>
