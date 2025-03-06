---
layout: project
title: "Diagnosing the Root Cause of ArduPilot Quadcopter Crashes"
permalink: /projects/uav_diagnosis/
---

# Root Cause of Quadrotor Failures

Imagine you are a professional photographer, and your beloved quadcopter, which you use to take breathtaking photos and videos, has crashed. What can you do to fix it?

First, you need to find the root cause. But all you know is that, in the middle of the flight, it suddenly stopped responding and fell to the ground. When you look at the altitude measurements you would see something like this:

<figure style="text-align: center; overflow: hidden; height: calc(100% - 6cm);">
    <img src="/assets/images/altitude_drop.png" 
         alt="altitude of quadrotor"
         style="width:800px;">
    <figcaption><em>Fig. 1 - Altitude of a quadrotor during a flight that ended in a crash.</em></figcaption>
</figure>


Now, what are your options for identifying the root cause and fixing your quadcopter before missing your next appointments?

There is an open-source tool called [LogAnalyzer](https://ardupilot.org/copter/docs/common-downloading-and-analyzing-data-logs-in-mission-planner.html) that is supposed to read ArduPilot flight logs and determine the root cause of the failure. But guess what? Thousands of users try it and still cannot figure out what went wrong. See [this](https://discuss.ardupilot.org/t/quad-sudden-descend-df-log-attached-help-needed-to-analyze/81251) example.

In [this](https://www.frontiersin.org/articles/10.3389/frobt.2024.1123762/full) and [this](https://ieeexplore.ieee.org/abstract/document/8688886/) paper, my colleagues and I argue that for effective root cause analysis, we first need to create causal graphs or fault trees. Once a causal graph or tree is ready, we use them in a process called actual causality analysis, in which all possible scenarios are examined to determine the true root cause of the UAV crash.

First, you need to create a causal graph, something like this:

<figure style="text-align: center; overflow: hidden; height: calc(100% - 6cm);">
    <img src="/assets/images/causal_graph.png" 
         alt="Causal graph of quadrotors"
         style="width:500px;">
    <figcaption><em>Fig. 2 - Causal Graph for quadrotors.</em></figcaption>
</figure>

Then, you need to use actual causality analysis to automatically check all scenarios where specific faults occurred or not. The Halpern-Pearl algorithm will handle this for you, identifying which leaf node is responsible for the root node failure. In the below example, the Extended Kalman Filter caused the quadrotor to crash.

<figure style="text-align: center; overflow: hidden; height: calc(100% - 6cm);">
    <img src="/assets/images/causal_graph_colored.jpg" 
         alt="Root cause analysis using the causal graph"
         style="width:700px;">
    <figcaption><em>Fig. 3 - Root cause analysis on the causal graph.</em></figcaption>
</figure>

You can refer to the above-mentioned papers to see our methodology for building such graphs by (1) scraping textual data from UAV websites using natural language processing techniques and (2) transforming architectural models of UAV control systems.