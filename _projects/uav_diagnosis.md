---
layout: project
title: "Diagnosing the root cause of Ardupilot quadcopter crashes"
permalink: /projects/uav_diagnosis/

---
# Root cause of UAV failures
Imagine you are a professional photographer and your lovely quadcopter which you use to take breath aking photos and videos has crashed. What can you do to fix it? first you need to find the root cause. All you know is that in the middle of the flight it just didnt listen to you and fell on the ground.
Now what are you options to find the root cause and fix your quadcopter before missing your next appointments?

There is a tool called LogAnalzyer which is supposed to read Ardupilot flight logs and tell the rootc cause of the failure. But guess what! there are tousands of users who try it and still could not figure our what was the cause. See [here](https://discuss.ardupilot.org/t/quad-sudden-descend-df-log-attached-help-needed-to-analyze/81251) for example.

In this paper me and my colleages argue that for an effective root cause analyis we need to first create causal graphs and then use them in a processes called actual casaulity analyisis, in which all scenraios are checked and the root cause of the UAV crash is determined.

First you need to create a causal graph somthing like this:

then you need to use the actual causality analyisis to  automatically check all scenarios where specific faults occured or not.

The Halpern-Pearl algorithms will check these for you and tell you which leaf node is the cause of the root node.

See the paper for more information.
