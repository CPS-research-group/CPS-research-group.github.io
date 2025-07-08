---
layout: single
author_profile: false
title: "INSPIRASI: Charging Optimization for Electric Vehicle Fleets"
sitemap: false
permalink: /inspirasi/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Staff/Students"
    text: "Rajeshkumar Ahir (Research Fellow) \n \n Michael Yuhas (Research Associate)"
---

******

# Research Motivation

The rapid transition toward sustainable urban transportation has accelerated the deployment of Electric Vehicles (EVs) in smart cities, offering a promising solution to reduce greenhouse gas emissions. However, this large-scale adoption introduces new complexities for both energy and transportation infrastructures. Numerous studies have explored EV integration into the grid, addressing charging station placement, battery degradation, and power load balancing. Recent literature emphasizes the need for smart, data-driven charging strategies that align with grid capacity, battery degradation, and user demand. Additionally, route optimization for EVs is gaining importance, as it directly impacts vehicle energy efficiency and user experience. Research also shows that external factors such as weather, terrain, and driving behavior significantly influence EV energy consumption and must be considered in optimization models. Despite these advances, current approaches often treat routing and charging independently or rely solely on either optimization or machine learning techniques, leading to suboptimal performance in real-world settings. 

The motivation for this research stems from the increasing adoption of EVs in logistics and transportation, and the pressing need for charging strategies that are cost-effective, battery health-aware, and grid-compliant. Through this initial exploration, we identified several key challenges that will guide our subsequent phases. These include handling grid limitations and demand response signals, addressing battery degradation from Vehicle to Grid (V2G) cycles and frequent fast-charging, coping with fluctuating electricity prices, and operating under limited infrastructure with constraints on charging ports and station capacities. Moreover, integrating V2G capabilities while ensuring the fulfillment of rental or operational demands presents a complex optimization problem.

# Problem Statement

This project addresses the gap by proposing an integrated framework that combines machine learning and mathematical optimization to tackle EV fleet charging and routing challenges holistically. The key problem is to develop intelligent algorithms that can schedule charging while considering grid constraints, battery health, V2G, service level constraints, and dynamic electricity pricing. Simultaneously, the framework must support route planning by focusing on understanding how variables such as EV model and range, weather conditions, terrain type, traffic conditions, vehicle load, battery load, and driving style impact energy consumption and, consequently, route feasibility. A significant limitation in existing models is the lack of real-time adaptability and personalized decision-making for diverse EV fleets. This research aims to overcome these limitations by developing hybrid, multi-factor models capable of capturing the operational intricacies of EVs in smart city (digital twin) environments.

# Research Objectives

This research addresses critical challenges of EV fleet charging and routing optimization. The primary research objectives proposed are as follows: 

* Development of smart hybrid algorithms (combining mathematical optimization and machine learning) to optimize the charging strategy for EVs while considering dynamics of the EV batteries and infrastructural limitations posed by the energy networks. 
* Development of pricing methodologies for demand responsive charging behavior of EV fleet. 
* Development of multi-factor models to capture the impact of weather conditions, terrain type, traffic conditions, vehicle load, battery load, and driving style on EV energy consumption and range. This will enable efficient route planning for EVs including intermediate charge planning. 

The above primary objectives will be realized in two phases below:  

## Phase 1: Development of Smart and Real-time Charge Scheduling Algorithm for EVs 

This phase addresses the first two research objectives by systematically investigating key challenges, including the dynamics of grid operations, the modeling and interpretation of EV driving behaviors, and the development of efficient battery models that incorporate degradation effects resulting from frequent charging and discharging cycles. Additionally, this phase explores the incorporation of dynamic demand response pricing mechanisms and the integration of V2G functionalities into the optimization framework. To investigate these challenges, the following set of tasks are designed: 

* Understanding the flaws and advantages of the existing EV and grid models (data-driven and physics based) and developing a hybrid model that will bring the advantages of both worlds. 
* Developing a centralized holistic learning-based charge scheduling framework considering several factors such as charging requirements, battery degradation, grid energy availability, uncertainties in the renewable sources at the charging station as well as environmental effects in terms of carbon footprint. 
* Generalizing the centralized approach into a decentralized learning control and power dispatch algorithm that is scalable and suitable for integration with Battery Management System (BMS), charging stations as well as the grid network. 
* To facilitate effective demand response in the EV fleet, we will formulate incentive mechanisms and dynamic pricing strategies utilizing game theory and multi-arm bandit reinforcement learning, considering the limitations posed by restricted resource capacity and shared storage at charging stations. 
* We will establish a framework for integrating Vehicle-to-Grid (V2G) and Vehicle-to-Vehicle (V2V) energy exchange capabilities within the developed scheduling algorithms. 

## Phase 2: Enhancing Feasibility Analysis for EVs through Multi-Factor Considerations in Route Planning including Charge Planning 

This phase addresses the third research objective. The major focus here is on understanding how variables such as EV model and range, weather conditions, terrain type, traffic conditions, vehicle load, battery load, and driving style impact energy consumption and, consequently, route feasibility. The main aim is to develop an integrated approach that will consider the prominent factors affecting energy consumption, charging stations availability and capacity and battery ageing, to address vehicle routing problems associated with large scale fleet operators. The approach will also aim towards incorporating ancillary grid services such as frequency regulation and peak load management in the problem formulation to evaluate the effectiveness of V2G and V2V from a high-level perspective. 

The following tasks will be executed to solve the above challenges: 

1. Conduct a comprehensive literature review to identify existing research on the influence of different factors on EV energy consumption and range. 
2. Collect fleet telematics data and charging station location and capacity data from work package 1 utilizing different sensors (data from the BlueBird Global EV taxi fleet). Analyse the impact of each variable (EV model, weather conditions, terrain type, traffic conditions, vehicle load, battery load, and driving style) on energy consumption and range. Explore case studies and simulations to observe the combined effects of multiple factors on route feasibility and costs. 
3. Develop a comprehensive model that considers the interplay of the above variables to enhance route planning for EVs. 
4. Apply and integrate the model with the Cognitive Digital Twin Platform to validate its effectiveness and accuracy. 

![image-right](/_pages/assets/inspirasi/overview.png){:height="60%" width="60%"}{: .align-right}
The full project description can be found [here](https://kemdiktisaintek.go.id/pengumuman/para-desainer-bersiaplah-kami-mengundang-kalian-untuk-ambil-bagian-untuk-berkarya-bersama-inspirasi-indonesia-ntu-singapore-institute-of-research-for-sustainability-and-innovation/){: .btn .btn--primary}.
