---
layout: single
author_profile: false
title: "Edge and Wireless Resource Allocation for Time-Sensitive Applications"
sitemap: false
permalink: /cloud/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
[//]: #  - title:
[//]: #    text: "[Open Positions](/cloud_open){: .btn .btn--primary}"
  - title: "Staff/Students"
    text: "Gao Chuanchao (PhD) \n \n Soumya Ranjan Sahoo (PhD) \n\n Manoj Kumar Lenka (PhD) \n\n Yagneshwar Dharmalingam (Engineer)"
---

******

# Research Motivation

Resource provisioning and scheduling for edge and cloud architectures have gained a lot of attention in the recent past both in academia and industry. This interest is primarily driven by the enormous success of two technologies in the field of computing: 1) Artificial Intelligence (AI), and 2) Internet of Things (IoT). Cloud architectures play a central enabling role for AI due to the significant demand that this technology imposes on computational resources. Orthogonally, IoT has enabled an unprecedented decentralization and deployment of services across domains, including several in which AI (at the edge) is gaining prominence. As a result, the edge and cloud hardware architecture is poised to dominate the field of computing across application domains in the future.

![image-right](/_pages/assets/cloud/architecture.png){:height="60%" width="60%"}{: .align-right}
The general objective of this project is to minimize the power consumption of end devices by offloading their computation intensive services on edge and cloud servers. Formulated as such, this problem has already received a lot of attention in the literature on mobile and edge computing. However, the originality of our work lies in the consideration of timing constraints associated with the services: in building energy management, most of the software services are indeed time-sensitive which means they have to be performed within predefined deadlines. This aspect has also been studied in a few research works, but most of them consider simplistic hypothesis when it comes to modelling timing interferences among services. The problem we propose to address is thus a resource allocation problem with the following objectives: (i) To minimize energy consumption of end devices; (ii) To minimize the average response times of non time-sensitive services; and (iii) To enforce end-to-end deadlines of time-sensitive services with probabilistic guarantees. As opposed to existing works, which study a subset of the infrastructure, we aim at a holistic approach taking into account (i) the wireless communication resources, (ii) the computation resources of edge and cloud servers and end devices, as well as (iii) the communication resources of the backhaul network. This problem is ambitious and will require finding a trade-off between optimality and reactivity: on the one hand, resource allocation problems are usually difficult to solve optimally because of their combinatorial complexity. On the other hand, service workload characteristics vary over time (notably because of mobility of devices), which means the resource allocation framework has to run online together with the system in order to adapt resource allocations to these variations.

In the past, due to limitations in wireless protocols and reliance on public cloud infrastructures, mainly non time-sensitive applications were deployed on edge and cloud architectures. This trend is changing however, both due to the proliferation of private cloud infrastructures as well as the development of reliable time-sensitive wireless protocols such as LoRa and 5G. Thus, there is a growing need for the deployment of time-sensitive applications on such architectures, which this project aims to facilitate. In a recent report titled “5G for business: a 2030 market compass” released by Ericsson, the global 5G-enabled market is projected to be USD 700 billion by 2030, with several potential time-sensitive applications in the key domains of manufacturing, energy and utilities, and automotive. Example applications include the following. 1) Running flexible production lines with remote operations through digital twins to accommodate reconfigurability for low-volume-high-mix production. 2) Collaborative robotics ensuring safe human-robot interactions. 3) Real-time operations and monitoring of distributed resources in urban energy systems. 4) Addressing safety concerns in driving automation systems like vision-based localization and perception through the use of reliable and low latency V2I (Vehicle-to- Infrastructure) communications. The results from this project are expected to be an enabling technology for the deployment of such safety-critical and time-sensitive applications across various domains.