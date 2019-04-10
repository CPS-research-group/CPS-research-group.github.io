---
layout: single
author_profile: false
title: "Towards Safe Machine Learning for CPS"
sitemap: false
permalink: /ml_safety/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Staff/Students"
    text: "Xiaozhe Gu (Research Fellow) \n \n Zahra RahimiNasab (PhD)"

  - title: "Former Staff/Students"
    text: " "
---

******

# Research Motivation

Machine learning (ML) techniques are increasingly influencing our lives, and moving into safety-critical applications. With the incorporated computational intelligence, these systems can have new capabilities such as self-learning and auto-diagnosis. For example, energy systems with ML modules can be more robust if they  can detect different types of false data injection attacks, smart building systems can greatly reduce economic costs if they can operate optimally under different situations , and vehicles can manoeuvre autonomously using efficient perception and localization techniques. Most of the above mentioned systems are safety-critical. Therefore, this raises the urgent need for ML safety. For example, in autonomous vehicles, an ML  based image classifier is often used to provide inputs to the software controlling electrical and mechanical subsystems. Since a false prediction of the classifier could be life-threatening, the safety of the resulting system must be guaranteed. In fact, a lack of such safety assurance is one of the primary reasons why these technologies are yet to find widespread adoption, and may even result in their premature death. 

******

# Our Solutions

### 1. Safe Fail

![image-left](/_pages/assets/ml_safety/tree.png){:height="50%" width="50%"}{: .align-right}
A practical technique for ML to avoid unsafe predictions is “Safe Fail”.  If a model is not likely to produce a correct output, a
reject option is selected, and the backup solution, a traditional non-ML approach or a human operator, for example, is applied, thereby causing the system to fail safely.  For example,  a support vector machine (SVM) like classifier with a reject option could be used for this purpose. The model will select a reject option if  classifier's predictive output $\phi(x)$ does not exceed a certain threshold. 

An implicit assumption made here is that the classifiers are most uncertain near the decision boundaries of different classes
and the distance from the decision boundary is inversely related to the confidence that an input instance belongs to a particular class.  This assumption is reasonable in some sense because the decision boundaries learnt by these models are usually located where many training samples with different labels overlap. However, if a feature space  contains few or no training samples at all, then the decision boundaries of ML models may wholly be based on an inductive bias, thereby having much epistemic uncertainty.  

ML models learn from a subset of possible scenarios that could be encountered operationally. Thus, they can only be as good as the
training examples they have learnt. Based on the observation that  ML models work well in the “training space” with a cloud of training points, but they could not extrapolate beyond the training space, we propose a feature space partition tree (FSPT) to split the initial feature space into multiple partitions with different densities of training data.  If  an input instance is from a feature space partition with no or few training samples,  then a reject option maybe selected.