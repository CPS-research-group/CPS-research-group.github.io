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

# Low-Criticality Execution Support for Mixed-Criticality System 

The existing mixed-criticality workload model has abstracted some key properties of mixed-criticality systems. However, it has received several criticisms that it makes unrealistic assumptions  as presented below.

1. Low-criticality tasks cannot be completely abandoned after an execution mode-switch,and should instead execute with degraded service as long as they do not affect the correctness of more critical tasks.
2. It is not reasonable to trigger an execution mode-switch and immediately suspend or degrade service to all the low-criticality tasks once a high-criticality task exceeds its low-confidence WCET estimation.
3. The WCET estimations in this model are primarily used as "budgets" for tasks. However, it is an undue burden on the application designer to derive these multiple WCET estimations for each task for this purpose.

To address these unrealistic assumptions, we first proposed a component based mixed-criticality model and a dynamic budget allocation scheme.


### 1. Component-based Technique for MC System 

![image-left](/_pages/assets/mc_scheduling/images/IMS.png){:height="50%" width="50%"}{: .align-right}

Our proposed component-based model for mixed-criticality systems  comprises a component-level design parameter called tolerance limit, which represents the expected number of high-criticality tasks within the component that will require additional resources at the same time. An execution strategy based on this parameter is also proposed, such that as long as WCET exceedance events are within the tolerance limit, low-criticality tasks in other components remain unaffected between internal mode-switch (IMS) and external mode-switch (EMS). Thus, the component boundaries of the proposed model are designed to provide the isolation necessary to support the execution of low-criticality tasks, and at the same time guarantee the correctness of the high-criticality ones.

### 2. Dynamic Budget Management Scheme

![image-left](/_pages/assets/mc_scheduling/images/flow1.pdf){:height="40%" width="40%"}{: .align-right}
We propose a dynamic mixed-criticality task and scheduling model in which high-criticality task budgets are determined at run-time depending on the execution scenario. To ensure a safe execution for all the high-criticality tasks, resources are always guaranteed to them upto their WCETs, a single value provided by the application designer. Off-line, we use schedulability analysis to determine a total budget allocation (single value) for all the high-criticality tasks combined. Execution mode-switch occurs in this model only when the resource utilization of all the high-criticality asks collectively exceed this total budget. At run-time, we use a strategy to allocate budgets to individual high-criticality tasks, with the objective of postponing the execution mode-switch as much as possible.


******

# Multiprocessor Mixed Criticality Scheduling Algorithms

![image-left](/_pages/assets/mc_scheduling/images/multicore_mc.tiff){:height="50%" width="50%"}{: .align-right}
To meet the growing processing demands of mixed-criticality systems, multi-core processors are increasingly being deployed due to their SWaP characteristics. We design several algorithms for scheduling dual-criticality systems on a homogeneous multiprocessor platform. In a dual-criticality system, there are tasks of two criticality levels, namely low and high. The high-criticality tasks have two utilization values, low-criticality utilization for low mode and high-criticality utilization for high mode. Our algorithms are broadly classified as follows.

### 1. Global Scheduling
We propose the multi-rate fluid scheduling model for dual-criticality systems wherein each high-criticality task uses different execution rate in the high-criticality mode. The main intuition behind this model is that, immediately upon entering the high-criticality mode several, several high-criticality tasks may simultaneously require additional processing capacity. To efficiently manage this overload, the multi-rate model distributes the execution across several windows of fixed duration. By managing the execution rates in these windows, the multi-rate model is able to provide a higher average execution rate to each high-criticality task.

### 1. Partitioned Scheduling
We focus on the problem of designing efficient partitioning strategies for dual-criticality systems. We develop a partitioning strategy based on the principle of evenly distributing the difference between total high-criticality utilization and total low-criticality utilization for the critical tasks among all processors. A smaller utilization difference implies the additional demand of high-criticality tasks when the system switches from low to high mode is small. Thus, we distribute this utilization difference evenly across all processors. By balancing this difference, we are able to reduce the pessimism in uniprocessor mixed-criticality schedulability tests that are applied on each processor, thus improving overall schedulability.

### 1. Semi-Partitioned Scheduling
In the conventional mixed-criticality workload model, upon criticality change, the lower criticality tasks are penalized to guarantee resources for the higher criticality ones. However, in practice, penalizing lower criticality tasks have adverse effects and hence, the system is often under-utilized. In this work, we consider the problem of guaranteeing some service to the lower criticality tasks after the criticality change. We explore the semi-partitioned scheduling model in which the low criticality tasks executing on a processor are migrated to an another processor upon mode switch to improve the service offered to them in the high criticality mode. We consider a restricted migration model wherein only the low criticality tasks are allowed to migrate between processors. To keep the predictability of the high criticality tasks intact we do not allow them to migrate.
 
******


******
# Evaluation testbed & demonstration

![image-left](/_pages/assets/mc_scheduling/images/torcs_simulator.JPG){:height="50%" width="50%"}{: .align-right}

******

# References
<ol>
<li> Jaewoo Lee, Kieu-My Phan, Xiaozhe Gu, Jiyeon Lee, Arvind Easwaran, Insik Shin and Insup Lee, “Fluid Model-based Mixed-Criticality Scheduling on Multiprocessors", IEEE Real-Time Systems Symposium (RTSS) 2014. </li>
<li>X Gu, A Easwaran, KM Phan, I Shin, "Resource efficient isolation mechanisms in mixed-criticality scheduling,"  27th  Euromicro Conference on Real-Time Systems (ECRTS), 2015, 13-24.</li>
<li> Xiaozhe Gu and Arvind Easwaran, "Dynamic Budget Management with Service Guarantees for Mixed-Criticality Systems", IEEE Real-Time Systems Symposium (RTSS), 2016.
<li> Xiaozhe Gu and Arvind Easwaran, “Efficient Schedulability Test for Dynamic-Priority Scheduling of Mixed-Criticality Real-Time Systems", ACM Transactions on Embedded Computing Systems (accepted) </li>
<li>  Xiaozhe Gu and Arvind Easwaran, “Dynamic Budget Management and Budget Reclamation for Mixed-Criticality Systems", Real-Time Systems (Under review)</li>
<li> Jaewoo Lee, Saravanan Ramanathan, Kiew-My Phan, Arvind Easwaran, Insik Shin and Insup Lee, "MC-Fluid: Multi-core Fluid-based Mixed-Criticality Scheduling", IEEE Transactions on Computers, 2017. </li>
<li> Saravanan Ramanathan, Arvind Easwaran and Hyeonjoong Cho, "Multi-rate fluid scheduling of mixed-criticality systems on multiprocessors", Real-Time Systems, 2017 </li>
<li> Saravanan Ramanathan and Arvind Easwaran, "Utilization difference based partitioned scheduling of mixed-criticality systems", IEEE Design, Automation & Test in Europe Conference & Exhibition (DATE) 2017.</li>
</ol>
