---
layout: single
author_profile: false
title: "Cache Design for Predictability"
sitemap: false
permalink: /cache_designs/

sidebar:
  - title:
    text: "[Return @CPSGroup](/){: .btn .btn--primary}"
  - title: "Research Student"
    text: "Sriram Vasudevan (PhD)"

  - title: "Former Staff"
    text: "Mohammad Shihabul Haque (Postdoc)"
---

******

# Research Motivation

![image-left](/_pages/assets/cache_designs/images/Drawing1.png){:height="40%" width="40%"}{: .align-right}
To ensure timely completion of tasks, real-time systems perform schedulability analysis. This analysis takes the Worst Case Execution Time (WCET) of each task as input. To estimate a task's WCET bound offline, predicted behaviour of each level in the processor cache memory hierarchy, i.e., a safe upper bound for the number of cache misses encountered by the task, is required. However, when muticore processors are used, behaviour of each level in the cache hierarchy becomes extremely challenging to predict; firstly, because of the interdependency of concurrently running tasks, and secondly, because of sharing by the processing cores. To overcome this challenge, a pragmatic and efficient solution is desired.
{: .align-left}

******

# Our Approach

We investigate and design cache management-based opportunities to overcome the cache predictability challenge for multicores. One direction of our curent approach is designing cache replacement policies that (i) are easy-to-implement in conventional set-associative cache memories, (ii) enable private and/or shared cache behavior prediction using intuitive and simple mechanisms, (iii) make efficient utilization of cache space, and (iv) maintain minimal performance during fierce cache contention as well as during uneven cache utilization by the processing cores. Another direction is designing prefetching techniques that are suitable, efficient and pragmatic for multicore real-time systems.

### Shared caches

![image-left](/_pages/assets/cache_designs/images/Shared_Cache.jpg){:height="40%" width="40%"}{: .align-right}
We successfully designed the first version of a prediction and performance aware replacement policy for cache memories shared among multiple processing cores. We believe that the replacement policy is the first of its kind to make predictable partitioning feasible for shared caches. This policy solves the performance limitations and practicality issues reported for predictable partitioning in prior research.
{: .align-left}

### Private caches

![image-left](/_pages/assets/cache_designs/images/Reconfigurable.jpg){:height="60%" width="60%"}{: .align-right}
We designed a prediction and performance aware replacement policy, called VRAMCache, for non-unified private cache memories in inclusive cache hierarchy with write invalidate coherency protocol. The policy deploys a first of its kind low overhead conflict miss detection technique. Moreover, it utilizes a novel, pragmatic and easy-to-implement mechanism to reduce conflict misses when appropriate. Despite its dynamic replacement decisions to deal with conflict misses, Least Recently Used (LRU) single-core based cache behaviour prediction mechanisms can be used to predict its behaviour.

******

# Publications

    <ol>
	<li class="a">Mohammad Shihabul Haque and Arvind Easwaran, "Predictability and Performance Aware Replacement Policy PVISAM for Unified Shared Caches in Real-time Multicores", ACM & IEEE International Conference on Compilers, Architecture, and Synthesis for Embedded Systems (CASES), 2018 (published in IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD), Volume 37, Issue 11, Pages 2720-2731, November 2018).</li>
	<li class="a">Mohammad Shihabul Haque, Sriram Vasudevan, Nihar Sriram, Arvind Easwaran, Y.C. Tay and Akash Kumar, "A Self-Reconfiguring Cache Architecture to Improve Control Quality in Cyber Physical Systems", IEEE International Symposium on Real-Time Computing (ISORC), 2018.</li>	
	<li class="a">Nitin Shivaraman, Sriram Vasudevan and Arvind Easwaran, "Demo Abstract: Predictable SoC architecture based on COTS multi-core", Demo Session of IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS) 2016.</li>	
    </ol>

