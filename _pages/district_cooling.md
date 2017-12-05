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

# District Cooling Systems (DCS)

DCS systems satisfy the cooling demand in an area through the production and distribution of chilled water from a central location. The centralization of chilled water production can take advantage of economies of scale, increasing system efficiently. It also alleviates maintenance responsibilities of air-conditioning maintenance from customers connected to the system. With the growing demand for cooling in cities, DCS are becoming an increasingly attractive option.   

![image-left](/_pages/assets/district_cooling/District_cooling_system.png){:height="80%" width="80%"}{: .align-right}

# Problem statement

Identification of the optimal design and operation of DCS systems is not a trival task. The system's efficiency is affected by equipment sizing, operation practices, demand profiles, weather conditions and resource availability etc. Interconnectedness of the system components further complicate the optimization task. Current optimization work concerning DCS systems tend to only consider the mono-optimization of simplified models of chillers (they usually account for upwards of 60% of DCS energy consumption) operating at fixed efficiencies. There is hence a need, for a more comprehensive framework which not only considers more variables but also explore the corresponding impact of optimizating conflicting objectives (e.g. cost and efficiency). 

# Proposed methodology

The proposed methodology builds on previous work on District Heating Systems (DHS) design optimization. The decomposition optimization methodology was adopted and applied DCS. The approach decomposes the problem into 2 levels - Master (Genetic Algorithm, GA) and slave (Mixed Integer Linear Program, MILP). Such an approach reduces the variables and hence the search space handled by the GA, giving better convergence values. The following summarizes the main steps in the optimization procedure.

1. Identification of mathematical models for DCS components 
2. Linearizing / relaxing the model
3. Defining variables which make the models non-linear as variables at the Master level. 

![image-left](/_pages/assets/district_cooling/methodology.png){:height="100%" width="100%"}{: .align-right}

### Identification of mathematical models for DCS components

The main components for DCS broadly comprise of chillers, pumps, networks, cooling towers and heat exchangers. Hybrid models (empirical-analytical) are preferred as they can be calibrated using raw data and extrapolated beyond the data range.

### Linearizing / relaxing the model

Most mathematical models tend to involve complex mathematical equations making direct application of optimization techniques a difficult task. Furthermore, loading meta-heuristic algorithms with too many variables will negatively impact resolution time and quality. Generally, the slave optimizer should be made to handle as many variables as possible. That is made possible with the application of some of the following techniques:

1. Piecewise linearization 
2. Bilinear variable linearization 
3. Big M relaxation

### Defining variables which make the models non-linear as variables at the Master level

The residual variables which cannot be handled at the slave level are left to the meta-heuristic algorithm (GA). 

# References

