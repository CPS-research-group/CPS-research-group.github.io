---
layout: single
author_profile: false
title: "Mixed-Criticality Real-Time Scheduling"
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
---

******

# Research Motivation

A Mixed-Criticality System (MCS) is one that has two or more distinct criticality levels (for example safety critical, mission critical and low-critical). There are two conflicting trends in the development of these systems. One is that the safety assurance requirements are increasingly emphasized. The other is that more functionalities are implemented on integrated platforms due to size, weight and power (SWaP) constraints. The existing techniques reserve unreasonably large amounts of computational resources to ensure that every real-time task including those that are non-critical performs correctly under harsh circumstances. As a result, the computational resources are highly under-utilized. To overcome this limitation, mixed-criticality workload model was proposed, wherein all tasks are required to perform correctly under normal circumstances but only the critical tasks are required to perform correctly under harsh circumstances.

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

### 3. Mixed Criticality in Automotive Systems

![image-left](/_pages/assets/mc_scheduling/images/torcs_simulator.JPG)
Automotive companies are moving towards ECU consolidation where safety and non safety-critical functionalities are integrated into fewer but more powerful hardware. This has made automotive to evolve into a Mixed Criticality System (MCS). Functional safety standards such as ISO 26262 (for automotive) have specified the guidelines to achieve design requirements of hardware and software elements implementing safety and non-safety critical functionalities as Automotive Safety Integrity Levels (ASILs). A vast body of existing literature on MCS focusses on new system models to achieve the design requirements and the corresponding analysis to verify the real-time guarantees.

A major challenge is to come up with a system designer friendly and a computationally efficient MCS model for automotive with a support to achieve graceful degradation of software elements corresponding to lower critical functionalities under the occurrence of timing faults. A test bed was built in order to benchmark the performance of new system model with the existing ones. The testbed is an hardware in the loop platform with TORCS as the vehicle simulator and Texas Instruments Hercules Development Board as the ECU. Applications such as Collision Avoidance, Adaptive Cruise Control, Steering Control etc., are implemented as a set of tasks hosted under FreeRTOS.
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
