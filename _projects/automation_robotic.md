---
layout: project
title: Robotic Automation
permalink: /projects/automation_robotic/
---

# Automating a unscrewing scenrio using a robotic arm
With the maturization of advanced machine learning methods such as Reinforcement Learning, a new era of robotic automation is on the horizon.  
I initiated a personal project to experiment with the available technologies in this area.  

I used the **ROS 2 Jazzy** framework, **MoveIt 2**, **ros2_control**, and **Gazebo** libraries to automate the unscrewing of some screws using a robotic arm.  

You can find the source code on my GitHub page:  
[https://github.com/EhsanZibaei/RoboticArm](https://github.com/EhsanZibaei/RoboticArm)

In the following video, you can see how the robot is programmed to precisely move its head to the screw head and then return to its initial position:

<div style="text-align: center;">
    <video width="800" height="450" autoplay muted controls>
        <source src="/assets/videos/demo.webm" type="video/webm">
        Your browser does not support the video tag.
    </video>
    <figcaption>
        Motion planning for a robotic arm to unscrew some screws on a simulated box.
    </figcaption>
</div>