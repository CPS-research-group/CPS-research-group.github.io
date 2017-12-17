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

A Mixed-Criticality System (MCS) is a real-time system that comprises tasks having two or more distinct criticality levels (e.g., safety-critical and mission-critical). There are two conflicting trends in the design of such systems. One is that the safety assurance requirements are being increasingly emphasized. The other is that more functionalities are being implemented on integrated platforms due to size, weight and power (SWaP) constraints. Existing scheduling techniques reserve large amounts of computational resources to ensure that every real-time task, including those that are less critical, provide full service even under theoretical worst-case conditions (safety assurance). As a result, the computational resources are highly under-utilized in such systems. To overcome this limitation, the mixed-criticality real-time task and scheduling model was proposed, wherein all tasks are required to provide full service under normal (practical worst-case) conditions, but less critical tasks may only be able to provide degraded service under theoretical worst-case conditions.

****** 

# Our Solutions

### 1. Execution support for less critical tasks

![image-left](/_pages/assets/mc_scheduling/images/dy.png){:height="50%" width="50%"}{: .align-right}
In the conventional mixed-criticality task and scheduling model, the less critical tasks are heavily penalized under theoretical worst-case conditions in order to guarantee resources for the high critical tasks. However, in practice, penalizing the less critical tasks has adverse effects on performance. In this work, we consider the problem of guaranteeing some (potentially degraded) service from the less critical tasks even under theoretical worst-case conditions.

We have developed a component-based mixed-criticality task and scheduling model to address the above problem. The model comprises a component-level design parameter called _tolerance limit_, which represents the expected number of critical tasks within the component that will simultaneously require additional computational resources during extreme worst-case conditions. We have developed a scheduling strategy based on this parameter such that as long as the critical task requirements are within this limit, the less critical tasks in other components will continue to provide full service. Thus, the component boundaries of the proposed model are designed to provide the isolation necessary to support the execution of less critical tasks.

We have also developed a dynamic budget-based mixed-criticality task and scheduling model to address the above problem. In this model, high critical task budgets are determined at runtime depending on individual task execution requirements. Offline, we determine a total feasible budget allocation for all the high critical tasks combined under practical worst-case conditions. This budget is then efficiently managed online with the objective of providing as much computational resources as possible for the less critical tasks. To ensure safety even under theoretical worst-case conditions, the less critical tasks are degraded in the eventuality that the high critical task requirements exceed the allocated total budget.

### 2. Mixed-criticality scheduling for multicores

![image-left](/_pages/assets/mc_scheduling/images/example_multi.png){:height="85%" width="50%"}{: .align-right}
To meet the growing processing demands of mixed-criticality systems, multicore processors are increasingly being deployed due to their SWaP characteristics. In this work, we consider the problem of scheduling mixed-criticality systems on a homogeneous multicore processor platform.

We have developed a fluid execution rate based scheduling model to address the above problem. In this model, the less critical tasks execute using a single fractional execution rate and the critical tasks execute using two fractional rates. Execution rate of the critical tasks vary depending on whether the system is experiencing normal or extreme worst-case conditions. During extreme worst-case conditions, the critical tasks execute at a higher rate than they would do normally, and the less critical tasks are suspended. These task execution rates are determined offline using an efficient convex optimization formulation, and the resulting scheduling policy is shown to have an optimal speed up bound of 4/3. To further improve performance, we have also extended this model to allow the critical tasks to use multiple execution rates during extreme worst-case conditions. As multiple critical tasks simultaneously require additional resources in such conditions, using fine-grained management of their execution rates we are able to achieve a higher resource utilization.

We have also developed an efficient partitioning (task-to-core mapping) strategy to address the multicore scheduling problem. Under this strategy, the critical tasks are allocated based on the principle of distributing the addtional demand, i.e., the difference in resource requirements between normal and extreme worst-case conditions, evenly among all the cores. Less critical tasks are allocated using a simple first-fit strategy. By balancing this additional demand, we are able to reduce the pessimism in mixed-criticality schedulability tests that are applied on each core, thus improving overall schedulability.
<!---
your comment goes here
and here -->

<### 3. Mixed-criticality in automotive systems

![image-left](/_pages/assets/mc_scheduling/images/torcs_simulator.JPG){:height="40%" width="40%"}

****** 

# References
<ol>
<li>  Xiaozhe Gu and Arvind Easwaran, "Dynamic Budget Management and Budget Reclamation for Mixed-Criticality Systems", Real-Time Systems (Under review).</li>
<li> Xiaozhe Gu and Arvind Easwaran, "Efficient Schedulability Test for Dynamic-Priority Scheduling of Mixed-Criticality Real-Time Systems", ACM Transactions on Embedded Computing Systems, 2017.</li>
<li> Saravanan Ramanathan, Arvind Easwaran and Hyeonjoong Cho, "Multi-rate fluid scheduling of mixed-criticality systems on multiprocessors", Real-Time Systems, 2017.</li>
<li> Jaewoo Lee, Saravanan Ramanathan, Kiew-My Phan, Arvind Easwaran, Insik Shin and Insup Lee, "MC-Fluid: Multi-core Fluid-based Mixed-Criticality Scheduling", IEEE Transactions on Computers, 2017.</li>
<li> Saravanan Ramanathan and Arvind Easwaran, "Utilization difference based partitioned scheduling of mixed-criticality systems", IEEE Design, Automation & Test in Europe Conference & Exhibition (DATE), 2017.</li>
<li> Xiaozhe Gu and Arvind Easwaran, "Dynamic Budget Management with Service Guarantees for Mixed-Criticality Systems", IEEE Real-Time Systems Symposium (RTSS), 2016.</li>
<li>Saravanan Ramanathan, Xiaozhe Gu and Arvind Easwaran, "The Feasibility Analysis of Mixed-Criticality Systems", Real-Time Scheduling Open Problems Seminar (RTSOPS), 2016.</li>
<li>Saravanan Ramanathan and Arvind Easwaran, "Evaluation of Mixed-Criticality Scheduling Algorithms using a Fair Taskset Generator", Workshop on Analysis Tools and Methodologies for Embedded and Real-time Systems (WATERS), 2016.</li>
<li> Sanjoy Baruah, Arvind Eswaran and Zhishan Guo, "MC-Fluid: simplified and optimally quantified", IEEE Real-Time Systems Symposium (RTSS), 2015.</li>
<li> Saravanan Ramanathan and Arvind Easwaran, "MC-Fluid: rate assignment strategies," Workshop on Mixed Criticality Systems (WMC), 2015.</li>
<li>Xiaozhe Gu, A Easwaran, KM Phan, I Shin, "Resource efficient isolation mechanisms in mixed-criticality scheduling," Euromicro Conference on Real-Time Systems (ECRTS), 2015.</li>
<li> Jaewoo Lee, Kieu-My Phan, Xiaozhe Gu, Jiyeon Lee, Arvind Easwaran, Insik Shin and Insup Lee, "Fluid Model-based Mixed-Criticality Scheduling on Multiprocessors", IEEE Real-Time Systems Symposium (RTSS) 2014.</li>
<li>  Xiaozhe Gu and Arvind Easwaran, "Optimal Speed-up Bound for 2-level Mixed-Criticality Arbitrary Deadline Systems", Real-Time Scheduling Open Problems Seminar (RTSOPS), 2014. </li>
</ol>
