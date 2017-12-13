---
layout: single
author_profile: false
title: "Optimization of District Cooling Systems"
permalink: /district_cooling/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Students"
    text: "Chiam Zhong Lin (PHD)"
---

******

# District Cooling Systems (DCS)

DCS satisfy the cooling demand in an area through the production and distribution of chilled water from a central location. The centralization of chilled water production can take advantage of economies of scale, increasing system efficiency. It also alleviates air-conditioning maintenance responsibilities from customers connected to the system. With the growing demand for cooling in cities, DCS are becoming an increasingly attractive option.   

![image-left](/_pages/assets/district_cooling/District_cooling_system.png){:height="50%" width="50%"}{: .align-right}

****** 

# Research Motivation

Optimal design and operation of DCS is a non-trival design-space exploration problem. The system's efficiency is affected by chiller sizing, operation practices, demand profiles, weather conditions, resource availability, thermal storage, etc. Interconnectedness of these system properties further complicate the problem. Current techniques for DCS design tend to only consider mono-optimization of simplified models of chillers operating at fixed efficiencies, although they usually account for more than 60% of energy consumption in a DCS. There is therefore a need for a more comprehensive framework which not only considers more design factors, but also explores the impact of optimizing conflicting objectives (e.g. cost and efficiency). Further, there is also a need to improve the operational efficiency of DCS based on weather and demand profile predictions.

****** 

# Proposed methodology

The proposed methodology builds on previous work related to optimization of District Heating Systems (DHS). This approach decomposes the complex problem into two dependent levels - Master (addressed using a Genetic Algorithm, GA), which drives the overall framework, and Slave (addressed using Mixed Integer Linear Program, MILP). Such an approach reduces the number of variables and hence the search space handled by the meta-heuristic GA, giving better convergence. The following summarizes the main steps in the optimization procedure.

1. Identification of mathematical models for DCS components.
2. Linearizing / Relaxing the models to make them suitable for the two-level optimization framework.

![image-left](/_pages/assets/district_cooling/methodology.png){:height="70%" width="70%"}{: .align-right}

### Modeling DCS components

The main components in a DCS comprise chillers, pumps, distribution network, cooling towers and heat exchangers. We develop hybrid models (empirical-analytical) for these components, as they can be calibrated using raw data and extrapolated beyond the data range.

### Linearizing / Relaxing the models

Most component models in a DCS tend to involve complex mathematical equations making direct application of optimization techniques a difficult task. Furthermore, loading meta-heuristic algorithms with too many variables will negatively impact resolution time and quality. Generally, the slave optimizer should be made to handle as many variables as possible. That is made possible in our approach with the application of some of the following techniques:

1. Piecewise linearization 
2. Bilinear variable linearization 
3. Big M relaxation

The residual variables which cannot be handled at the slave level are left to the meta-heuristic algorithm (GA).
