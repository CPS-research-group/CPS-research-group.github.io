---
layout: single
author_profile: false
title: "Scheduling Algorithms for Mixed-Criticality Systems"
header:
  image: /assets/graphics/mainBanner.png
  <!-- video:
    id: 78mwXSsyYlw
    provider: youtube -->
sitemap: false
permalink: /mc_scheduling/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Students"
    text: "Xiaozhe  Gu (PHD) \n \n Saravanan Ramanathan (PhD) \n \n Sundar Vijayakumar (PhD)"
    
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

# Motivation of Mixed Criticality Scheduling Theory
A mixed criticality system (MCS) is one that has two or more distinct criticality levels (for example safety critical, mission critical and low-critical). There are two conflicting trends in the development of these systems. One is that the safety assurance requirements are increasingly emphasized. The other is that more functionalities are implemented on integrated platforms due to size, weight and power (SWaP) constraints. The existing techniques reserve unreasonably large amounts of computational resources to ensure that every real-time task including those that are non-critical performs correctly under harsh circumstances. As a result, the computational resources are highly under-utilized. To overcome this limitation, mixed-criticality workload model was proposed, wherein all tasks are required to perform correctly under normal circumstances but only the critical tasks are required to perform correctly under harsh circumstances.

****** 

# Proposed methodology

### 1. Low-Criticality Execution Support
![image-left](/_pages/assets/mc_scheduling/images/IMS.png){:height="50%" width="50%"}{: .align-right}
In the conventional mixed-criticality workload model, upon criticality change, the lower criticality tasks are penalized to guarantee resources for the higher criticality ones. However, in practice, penalizing lower criticality tasks have adverse effects and hence, the system is often under-utilized. In this work, we consider the problem of guaranteeing some service to the lower criticality tasks after the criticality change.

We propose a component-based model for dual-criticality (namely low and high) systems which comprises a component-level design parameter called tolerance limit, which represents the expected number of high-criticality tasks within the component that will require additional resources at the same time. We propose an execution strategy based on this parameter such that as long as the high-criticality switch instances are with in this limit, the low-criticality tasks in other components remain unaffected. Thus, the component boundaries of the proposed model are designed to provide the isolation necessary to support the execution of low-criticality tasks.

We also propose a dynamic mixed-criticality task and scheduling model in which high-criticality task budgets are determined at run-time depending on the execution scenario. To ensure a safe execution for all the high-criticality tasks, resources are always guaranteed to them after the criticality change. Offline, we determine a total budget allocation for all the high-criticality tasks combined. The criticality change occurs only when the resource utilization of all the high-criticality asks collectively exceed this total budget. At run-time, we use a strategy to allocate budgets to individual high-criticality tasks, with the objective of postponing the execution mode-switch as much as possible.
{: .align-left}

### 2. Multi-core Mixed Criticality Scheduling
![image-left](/_pages/assets/mc_scheduling/images/multicore_mc.jpg){:height="50%" width="50%"}{: .align-right}
To meet the growing processing demands of mixed-criticality systems, multi-core processors are increasingly being deployed due to their SWaP characteristics. In this work, we design algorithms for scheduling dual-criticality systems on a homogeneous multi-core processor platform.  In a typical dual-criticality system, upon criticality change several high-criticality tasks demand for additional processing resource. To efficiently manage this overload, we propose the multi-rate model that distributes the high-criticality execution across several windows of fixed duration. By managing the execution rates in these windows, the multi-rate model is able to provide a higher average execution rate to each high-criticality task. We also propose an efficient task-to-core mapping strategy for dual-criticality systems based on the principle of evenly distributing this addtional demand among all processors. By balancing this demand, we are able to reduce the pessimism in uniprocessor dual-criticality schedulability tests that are applied on each processor, thus improving overall schedulability.
{: .align-left}

### 3. Evaluation testbed & demonstration

![image-left](/_pages/assets/mc_scheduling/images/torcs_simulator.JPG){:height="50%" width="50%"}{: .align-right}
{: .align-left}

******

# References
<ol>
<li>  Xiaozhe Gu and Arvind Easwaran, “Dynamic Budget Management and Budget Reclamation for Mixed-Criticality Systems", Real-Time Systems (Under review).</li>
<li> Xiaozhe Gu and Arvind Easwaran, “Efficient Schedulability Test for Dynamic-Priority Scheduling of Mixed-Criticality Real-Time Systems", ACM Transactions on Embedded Computing Systems (accepted).</li>
<li> Saravanan Ramanathan, Arvind Easwaran and Hyeonjoong Cho, "Multi-rate fluid scheduling of mixed-criticality systems on multiprocessors", Real-Time Systems, 2017.</li>
<li> Jaewoo Lee, Saravanan Ramanathan, Kiew-My Phan, Arvind Easwaran, Insik Shin and Insup Lee, "MC-Fluid: Multi-core Fluid-based Mixed-Criticality Scheduling", IEEE Transactions on Computers, 2017.</li>
<li> Saravanan Ramanathan and Arvind Easwaran, "Utilization difference based partitioned scheduling of mixed-criticality systems", IEEE Design, Automation & Test in Europe Conference & Exhibition (DATE) 2017.</li>
<li> Xiaozhe Gu and Arvind Easwaran, "Dynamic Budget Management with Service Guarantees for Mixed-Criticality Systems", IEEE Real-Time Systems Symposium (RTSS), 2016.</li>
<li>X Gu, A Easwaran, KM Phan, I Shin, "Resource efficient isolation mechanisms in mixed-criticality scheduling,"  27th  Euromicro Conference on Real-Time Systems (ECRTS), 2015, 13-24.</li>
<li> Jaewoo Lee, Kieu-My Phan, Xiaozhe Gu, Jiyeon Lee, Arvind Easwaran, Insik Shin and Insup Lee, “Fluid Model-based Mixed-Criticality Scheduling on Multiprocessors", IEEE Real-Time Systems Symposium (RTSS) 2014.</li>
</ol>
