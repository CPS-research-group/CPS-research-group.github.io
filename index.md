---
layout: single
author_profile: true
header:
  image: /assets/graphics/mainBanner.png
  
sidebar:

  - title: "Research Staff"
    text: "
Melanie Mille (Research Intern)\n\n
Peeterson E. R. Jose (Engineer)\n\n
Daniel Ng Jun Xian (Engineer)"

  - title: "Research Students"
    text: "
Gao Chuanchao (PhD) \n\n
Michael Yuhas (PhD)\n\n
Mainak Dan (PhD) \n\n
Nitin Shivaraman (PhD, joint with Sebastian Steinhorst - TUM)\n\n
Ankita Samaddar (PhD)\n\n
Zahra Rahimi Nasab (PhD)"

  - title: "Former Postdocs/Students"
    text: "
Yeli Feng (ST Engineering, Singapore) \n\n    
Sundar Vijayakumar (IIT-M, India) \n\n
Seima Suriyasekaran (SIT, Singapore) \n\n
Sriram Vasudevan (SUTD, Singapore) \n\n
Zhiheng Xu (Dyson, Singapore)\n\n
Omar Al-Bataineh (NUS, Singapore)\n\n
Chiam Zhonglin (Zyllem, Singapore)\n\n
Saravanan Ramanathan (NTU, Singapore)\n\n
Xiaozhe Gu (CUHK, Shenzhen, China)\n\n
Shihabul Haque (I2R, A*STAR, Singapore)\n\n
Sidharta Andalam (Bosch Corporate Research, Singapore)\n\n
Bai Xue (Chinese Academy of Sciences, China)\n\n
Arpita Bhattacharjee (Mercedes Benz R&D, India)"
---

******

# Overview
Cyber-Physical Systems (CPS) encompass systems in which the cyber world of computation and communication closely interacts with the physical world of sensors and actuators. These are highly networked and deeply embedded systems such as those found in modern day aircrafts, automotives, factories, medical devices, smart phones, electric grids, etc. From driver-less cars and air traffic management using sense and avoid, to plug-and-play operating rooms and smart electric grids that integrate traditional and renewable energy sources, intelligent automation of an enormous scale is finding its way into many of these systems.

Primary interests of the CPS Research Group @SCSE,NTU are in the design and analysis of safety-critical and time-critical CPS, with a particular focus on cyber-resource management and safety assurance. The current research themes can be broadly classified as follows:

<ol>
<li>Resource Management and Scheduling</li>
<li>Safety Assurance in Learning Enabled Components</li>
</ol>
******

# Ongoing Projects

******

## DesCartes: Intelligent Modelling for Decision-making in Critical Urban Systems

![image-right](/assets/graphics/descartes.png){:height="50%" width="50%"}{: .align-right}
A new Hybrid Artificial Intelligence (HAI) program has been launched through an international collaboration involving the French National Centre for Scientific Research (CNRS), the Agency for Science, Technology and Research (A*STAR), Nanyang Technological University (NTU) and the National University of Singapore (NUS). This program will develop solutions that support the creation of "Smart Cities", including development of hybrid AI methods that aim to enhance real-time decision-making in urban-critical systems, with a focus on individuals and society at large. It will also adopt a holistic and multidisciplinary approach that combines AI with existing subject-based models from physics and engineering.

Within this large program, our research will focus on the "Augmented Hybrid Engineering" work package, that brings  the  engineering,  technological,  and  application dimensions to the concept of HAI. It aims at proposing operational methodology and architecture, from smart sensing and predictive diagnostics to robust and scalable control, for critical and complex system-of-systems. This implies a multi-disciplinary  consortium  with complementary expertise between France and Singapore. The   disruptive engineering developments, implementations and integrations performed in this work package will permit to reach the project final objectives in terms of  relevant and reliable technologies that are fully integrated and validated on representative proofs-of-concept and real-life systems.

*CNRS@CREATE (National Research Foundation, Singapore)*

[Program Overview (external link)](https://www.cnrsatcreate.cnrs.fr/descartes/){: .btn .btn--primary}

[Read More (Augmented Hybrid Engineering)](/descartes){: .btn .btn--primary}

## Trust to Train and Train to Trust: Agent Training Programs for Safety-Critical Environments

![image-right](/assets/graphics/atp.png){:height="40%" width="40%"}{: .align-right}
Over the last few years, Artificial Intelligence (AI) systems have achieved super-human performance in specific yet complex tasks across diverse environments (e.g., image recognition, language translation, complex games like Go). Given their effectiveness, we aim to employ AI (or Agent) Training Programs (ATPs) to generate scenarios automatically for training (on specific tasks) in safety-critical applications while addressing the issue of trust to improve adoption:

- Trust to Train: Gain trust of organizations employing ATPs through guarantees on training outcomes (safety), equality in training for all trainees (fairness), and training for unexpected situations (robustness).  

- Train to Trust: Explainable (understandable) and effective feedback interface in training to gain trust of trainees.  

We intend to develop and assess Explainable and tRustworthy (ExpeRt) ATPs with feedback interfaces to adaptively train human(s) for safety-critical applications with show-case projects on emergency response and maritime navigation. This project is a collaboration between faculty at Singapore Management University (SMU), National University of Singapore (NUS) and Nanyang Technological University (NTU). Within the trustworthiness assurance research track in the above project, in our research we will be exploring techniques for assessing the safety, robustness and fairness properties in deep reinforcement learning (dRL) frameworks used in the ATPs.

*AI Singapore Research Programme (AI Singapore, Singapore)*

[Read More](/pac_verification){: .btn .btn--primary}

## Assured-Safety Architecture for Machine Learning based CPS

![image-right](/assets/graphics/mlsafety.png){:height="40%" width="40%"}{: .align-right}
Machine learning (ML) techniques are increasingly applied to decision-making and control problems in CPS among which many are safety-critical, e.g., chemical plants, robotics, autonomous vehicles. Despite the significant benefits brought by ML techniques, there are various factors  that can impede the achievement of ML safety. For example, 1) expressive ML models such as deep neural networks (DNN) are typically considered to be non-transparent, behaving as a “black-box” and lacking interpretable knowledge representation; 2) The empirical risk minimization approach used to train ML models reduces the probability of false prediction on the assumption that the training samples are drawn from the actual underlying probability distribution of the population; 3) Formal verification requires a specification of the property of interest, i.e., a precise, mathematical statement of what the system is supposed to or not supposed to do. However, it is difficult to come up with such a formal specification for ML-CPS. In this work, we focus on the design of novel techniques to improve the safety of ML-CPS. In particular, we develop online and robust detection techniques for Out-of-Distribution (OOD) data and Probably Approximately Correct (PAC) techniques for deriving probabilistic testing guarantees in ML-CPS.

*Tier-2 Grant (Ministry of Education, Singapore)*

*Delta-NTU Cyber-Physical Systems Corporate Lab (National Research Foundation, Singapore and Delta Electronics Inc.)*

*Urban Mobility Grand Challenge (ERI@N, NTU through Land Transport Authority and National Research Foundation, Singapore)*

[Read More](/ml_safety){: .btn .btn--primary}

******

# Past Projects

******

## Operational Optimization for Energy Management Systems

![image-right](/assets/graphics/controlHeating.png){:height="40%" width="40%"}{: .align-right}

In Singapore, the operation of buildings consumes about a third of total electricity, making them one of the largest consumers of primary energy. A significant portion of this energy is consumed by space cooling and dehumidification. Thus, the reduction and more efficient use of energy in buildings will provide a large leverage for climate change mitigation. Orthogonally, given its geographical constraints, access to renewable sources of energy such as solar and wind will be minimal relative to its needs. Hence a significant focus is also expected on the electrification of its automotive fleet to reduce reliance on traditional sources of energy. In this work, we develop IoT methodologies and optimization frameworks for decentralized monitoring of energy use in urban environments as well as for the operational optimization of such interconnected and complex energy systems.           

*Industrial PhD Grant (Economic Development Board, Singapore and Veolia City Modelling Center)*

*PhD Grant (ERI@N, NTU)*

*Intra-CREATE Seed Grant (National Research Foundation, Singapore and TU Munich)*

[Read More](/energy_optimization){: .btn .btn--primary}

## Model-in-the-Loop Framework for Manufacturing

![image-left](/assets/graphics/cpsModellingLogo.png){:height="40%" width="40%"}{: .align-left}
With sensing technology becoming pervasive in manufacturing plants, large amounts of data are being generated in real-time. As a consequence, there is a need to effectively utilize this _big data_ so that the desired objectives of Industry 4.0 such as predictive maintenance, root cause analysis and re-configurability, can be realized. The digital twin, obtained by using this big data together with plant and controller models, can be viewed as an accurate and time-synchronized characterization of the physical system in the cyber space. In this work, we aim to develop a tooling framework to realize the design and deployment of a digital twin in manufacturing with the following objectives: introducing a software architecture for the digital twin construction and application development, building a digital twin using heterogeneous modeling formalisms and online data integration, and providing a single source of truth for isolated applications via well-formed interfaces.

*Delta-NTU Cyber-Physical Systems Corporate Lab (National Research Foundation, Singapore and Delta Electronics Inc.)*

[Read More](/digital_twin){: .btn .btn--primary}

## Resilient Cyber-Infrastructure for Manufacturing

![image-left](/assets/graphics/resilienceLogo.png){:height="40%" width="40%"}{: .align-left}
Sensor proliferation and large-scale connectivity have enabled a variety of functionalities in CPS. However, connectivity also means that these systems operate in unreliable open environments, and hence resiliency to faults become important. This resiliency is fundamentally dependent on the resiliency of the cyber-infrastructure (communication network and computation nodes), which plays a central role of data delivery and execution of control. The objective of this work is to design a scalable and runtime-configurable resilience management framework for fault-handling in such emerging CPS. We also aim to demonstrate these capabilities through case studies in the application domain of smart manufacturing.

*Delta-NTU Cyber-Physical Systems Corporate Lab (National Research Foundation, Singapore and Delta Electronics Inc.)*

[Read More](/resilience_cps){: .btn .btn--primary}

## Mixed-Criticality Scheduling Algorithms

![image-right](/assets/graphics/time2task.png){:height="40%" width="40%"}{: .align-right}
With increasing functionality and automation in real-time systems, the computational demand is steadily increasing, while resources available for servicing this demand are limited due to size, weight and power restrictions. As a result a module integration trend has emerged, so that many different applications are being cohosted on the same processing unit. Some of these applications are extremely critical for the correct behavior of the system (e.g., collision avoidance in automotive), while some others are relatively less critical (e.g., hill assist in automotive), thus giving rise to mixed-criticality real-time systems. In this work, we focus on the design of single-core as well as multi-core scheduling algorithms for such systems. We also develop practical workload models to characterize such systems, and evalute the same using an automotive testbed.

*Tier-2 Grant (Ministry of Education, Singapore)*

[Read More](/mixed_criticality){: .btn .btn--primary}

## Cache Designs for Timing-Predictability

![image-right](/assets/graphics/Cache2Predict.png){:height="40%" width="40%"}{: .align-right}
Cache memory plays a key role for performance improvement and energy efficiency in modern computer systems. However, when used as a shared resource in a multicore system, cache memory becomes the key source for timing unpredictability. As predictability is a major concern in real-time systems, this work designs cache memories to address this issue. We focus on the development of hardware techniques, including cache replacement policy designs, to improve the predictability of both private as well as shared caches on multicores.

*Tier-1 Grant (Ministry of Education, Singapore)*

[Read More](/cache_designs){: .btn .btn--primary}



