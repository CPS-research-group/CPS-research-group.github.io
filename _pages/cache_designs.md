---
layout: single
author_profile: false
title: "Cache Design for Predictability"
sitemap: false
permalink: /cache_designs/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Staff/Student"
    text: "Mohammad Shihabul Haque (Postdoc)\n\n
    	   Sriram Vasudevan (PhD)"
---

******

# Research Motivation

![image-left](/_pages/assets/cache_designs/images/Drawing1.png){:height="40%" width="40%"}{: .align-right}
To ensure timely completion of tasks, real-time systems perform schedulability analysis. This analysis takes the Worst Case Execution Time (WCET) of each task as input. To estimate a task's WCET bound offline, predicted behaviour of each level in the processor cache memory hierarchy, i.e., a safe upper bound for the number of cache misses encountered by the task, is required. However, when muticore processors are used, behaviour of each level in the cache hierarchy becomes extremely challenging to predict; firstly, because of the interdependency of concurrently running tasks, and secondly, because of sharing by the processing cores. To overcome this challenge, a pragmatic and efficient solution is desired.
{: .align-left}

******

# Contributions

We investigate and design cache management-based opportunities to overcome the cache predictability challenge for multicores. One direction of our curent approach is designing cache replacement policies that (i) are easy-to-implement in conventional set-associative cache memories, (ii) enable private and/or shared cache behavior prediction using intuitive and simple mechanisms, (iii) make efficient utilization of cache space, and (iv) maintain minimal performance during fierce cache contention as well as during uneven cache utilization by the processing cores. Another direction is designing prefetching techniques that are suitable, efficient and pragmatic for multicore real-time systems.

### 1. Shared caches

![image-left](/_pages/assets/cache_designs/images/Shared_Cache.jpg){:height="40%" width="40%"}{: .align-right}
We successfully designed the first version of a prediction and performance aware replacement policy for cache memories shared among multiple processing cores. We believe that the replacement policy is the first of its kind to make predictable partitioning feasible for shared caches. This policy solves the performance limitations and practicality issues reported for predictable partitioning in prior research.
{: .align-left}

### 2. Private caches

![image-left](/_pages/assets/cache_designs/images/Reconfigurable.jpg){:height="60%" width="60%"}{: .align-right}
We designed a prediction and performance aware replacement policy, called VRAMCache, for non-unified private cache memories in inclusive cache hierarchy with write invalidate coherency protocol. The policy deploys a first of its kind low overhead conflict miss detection technique. Moreover, it utilizes a novel, pragmatic and easy-to-implement mechanism to reduce conflict misses when appropriate. Despite its dynamic replacement decisions to deal with conflict misses, Least Recently Used (LRU) single-core based cache behaviour prediction mechanisms can be used to predict its behaviour.



