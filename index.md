---
layout: single
author_profile: true
header:
  image: /assets/graphics/mainBanner.png
  
sidebar:

  - title: "Research Staff"
    text: "
Sidharta Andalam (RF)\n\n
Mohammad Shihabul Haque (RF)\n\n
Daniel Ng Jun Xian (RA)"

  - title: "Research Students"
    text: "
Xiaozhe Gu (PhD)\n\n
Saravanan Ramanathan (PhD)\n\n
Sriram Vasudevan (PhD)\n\n
Sundar Vijayakumar (PhD)\n\n
Chiam Zhong Lim (PhD)\n\n
Ankita Sammadar (PhD)\n\n
Daniel Ng Jun Xian (MEngg)"

  - title: "Former Staff/Students"
    text: "
Bai Xue (Chinese Academy of Sciences, China)\n\n
Arpita Battacharjee (Axiscades Engineering Technologies, India)"

realtime:
  - image_path:
    title: "Mixed-Criticality Scheduling Algorithms"
    excerpt: "With increasing functionality and automation in real-time systems, the computational demand is steadily increasing, while resources available for servicing this demand are limited due to size, weight and power restrictions. As a result a module integration trend has emerged, so that many different applications are being cohosted on the same processing unit. Some of these applications are extremely critical for the correct behavior of the system (e.g., collision avoidance in automotive), while some others are relatively less critical (e.g., hill assist in automotive), thus giving rise to mixed-criticality real-time systems. In this project, we focus on the design of single-core as well as multi-core scheduling algorithms for such systems. We also develop practical workload models to characterize such systems, and evalute the same using an automotive testbed. \n\n
	**Tier-2 Grant (Ministry of Education, Singapore)**"
    url: "mc_scheduling"
    btn_label: "Read More"
    btn_class: "btn--inverse"
---

******

# Overview
Cyber-Physical Systems (CPS) encompass systems in which the cyber world of computation and communication closely interacts with the physical world of sensors and actuators. These are highly networked and deeply embedded systems such as those found in modern day aircrafts, automotives, factories, medical devices, smart phones, electric grids, etc. From driver-less cars and air traffic management using sense and avoid, to plug-and-play operating rooms and smart electric grids that integrate traditional and renewable energy sources, intelligent automation of an enormous scale is finding its way into many of these systems.

Current interests of the CPS Research Group @SCSE,NTU are in the design of cyber-infrastructures for CPS, especially for systems with time-critical functionalities (i.e., real-time systems). The research themes can be broadly classified as follows:

<ol>
<li>Real-Time Systems (scheduling algorithms and hardware designs)</li>
<li>Model-based Design Methodologies (for resilience and operational efficiency)</li>
<li>Energy Management (scheduling algorithms)</li>
</ol>

******

# Real-Time Systems

******

### Mixed-Criticality Scheduling Algorithms

![image-right](/assets/graphics/time2task.png){:height="50%" width="50%"}{: .align-right}
With increasing functionality and automation in real-time systems, the computational demand is steadily increasing, while resources available for servicing this demand are limited due to size, weight and power restrictions. As a result a module integration trend has emerged, so that many different applications are being cohosted on the same processing unit. Some of these applications are extremely critical for the correct behavior of the system (e.g., collision avoidance in automotive), while some others are relatively less critical (e.g., hill assist in automotive), thus giving rise to mixed-criticality real-time systems. In this project, we focus on the design of single-core as well as multi-core scheduling algorithms for such systems. We also develop practical workload models to characterize such systems, and evalute the same using an automotive testbed.

*Tier-2 Grant (Ministry of Education, Singapore)*

[//]: # [Read More](/mc_scheduling){: .btn .btn--inverse}

[//]: # ### Cache Designs for Timing-Predictability

[//]: # ![image-right](){:height="50%" width="50%"}{: .align-right}

[//]: # *Tier-1 Grant (Ministry of Education, Singapore)*

[//]: # [Read More](/cache_designs){: .btn .btn--inverse}

******

# Model-based Design Methodologies

******

### Resilient Cyber-Infrastructure for Manufacturing

![image-left](/assets/graphics/resilienceLogo.png){:height="50%" width="50%"}{: .align-left}
Sensor proliferation and large-scale connectivity have enabled a variety of functionalities in CPS. However, connectivity also means that these systems operate in unreliable open environments, and hence resiliency to faults and attacks become important. This resiliency is fundamentally dependent on the resiliency of the cyber-infrastructure (communication network and computation nodes), which plays a central role of data delivery and execution of control. The objective of this project is to design a resilient cyber-infrastructure for such emerging CPS. A smart manufacturing testbed is also built to demonstrate the capabilities developed in the project.

*Delta-NTU Cyber-Physical Systems Corporate Lab (National Research Foundation, Singapore and Delta Electronics Inc.)*

[Read More](/resilience_cps){: .btn .btn--primary}

### Model-in-the-Loop Framework for Manufacturing

![image-left](/assets/graphics/cpsModellingLogo.png){:height="60%" width="50%"}{: .align-left}
With sensing technology becoming pervasive in manufacturing plants, large amounts of data are being generated in real-time. As a consequence, there is a need to effectively utilize this _big data_ so that the desired objectives of Industry 4.0 such as predictive maintenance and re-configurability, can be realized. The cyber twin, obtained by using this big data together with plant models, can be viewed as an accurate and time-synchronized characterization of the physical system in the cyber domain. In this project, we aim to develop a tooling framework to realize the design and deployment of a cyber twin in manufacturing with the following objectives: plant and controller model specification and simulation, and automatic model-to-code transformation for controller and cyber twin synthesis.

[//]: # *Delta-NTU Cyber-Physical Systems Corporate Lab (National Research Foundation, Singapore and Delta Electronics Inc.)*

[Open Positions](/model_in_loop){: .btn .btn--primary}

******

# Energy Management

******

### Optimization Framework for District Cooling Systems

![image-right](/assets/graphics/controlHeating.png){:height="50%" width="50%"}{: .align-right}
In Singapore, the operation of buildings consumes about 37% of total electricity, making them one of the largest consumers of primary energy. Around 70% of the energy used in buildings is consumed by space cooling and dehumidification. Thus, the reduction and more efficient use of energy for cooling in buildings will provide a large leverage for climate change mitigation. District cooling systems that supply such cooling energy from centralized chillers via distribution networks within a geographical area have emerged as an efficient alternative to personalized air-conditioning systems. Although such cooling systems are in commercial use globally, significant operational inefficiencies and losses are often reported. Towards mitigating these inefficiencies, in this project, we develop a design methodology for formal modelling and operational optimization of district cooling systems.

*Industrial PhD Grant (Economic Development Board, Singapore and Veolia City Modelling Center)*

[//]: # [Read More](/district_cooling){: .btn .btn--inverse}

### Distributed and Internet-of-Things (IoT) based Electricity Metering and Load Management

![image-right](/assets/graphics/smart_metering.png){:height="50%" width="50%"}{: .align-right}
The aim of this project is to implement the concept of decentralized electricity metering and load management using IoT capabilities in smart devices. The long-term objective is to remove household- or company-level smart electricity metering and replace it with aggregated reporting of all devices in the household/company environment. Moreover, this approach will also enable these electricity-consuming devices to participate in a deregulated electricity market. By developing approaches from the blockchain technology domain towards application in embedded devices, a trustless authentication mechanism for provisioning and verifying the compliance of these devices will be made possible. Our investigation of how to achieve a fully decentralized energy grid with smart contracts, binding all grid participants to system-level goals, will contribute to bringing smart grid functionality to a level of granularity previously not possible.

*Intra-CREATE Seed Grant (National Research Foundation, Singapore and TU Munich)*
