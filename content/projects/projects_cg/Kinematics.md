---
author: "Ying-Shan Chen"
title: "Forward and Inverse Kinematics"
date: '2026-04-15'
categories: [
    "Computer Graphics",
    "Practice"
]
tags: [
    "Computer Graphics",
    "Optimization Method",
    "C++"
]
description: "Implement forward and inverse kinematics motion."
---
🔗 See more details about <a href="https://github.com/ChenYingShan1114/Forward-and-Inverse-Kinematics">kinematics</a>, forked from the projects in computer graphics course at University of Toronto.

## Forward Kinematic

Provide keyframes and use Catmull-Rom interpolation to simulate animation.

* ### robot arm

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/robot-arm-forward.mp4" controls type="video/mov" width="600"></video>
</p>

* ### chimpanzee hand

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/chimpanzee-hand-forward.mp4" controls type="video/mov" width="600"></video>
</p>

## Inverse Kinematic

Users interact with the endpoints of each bone, and the Levenberg-Marquardt algorithm is used to optimize the results.

* ### robot arm

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/robot-arm-inverse.mp4" controls type="video/mov" width="600"></video>
</p>

* ### chimpanzee hand

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/chimpanzee-hand-inverse.mp4" controls type="video/mov" width="600"></video>
</p>

* ### ikea lamp

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/ikea-lamp-inverse.mp4" controls type="video/mov" width="600"></video>
</p>

* ### knight

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/knight-inverse.mp4" controls type="video/mov" width="600"></video>
</p>

* ### beast

<p align="center">
    <video src="/self/mp4/projects_cg/Kinematics/beast-inverse.mp4" controls type="video/mov" width="600"></video>
</p>


## Reference
1. <a href="https://en.wikipedia.org/wiki/Catmull–Rom_spline">Catmull–Rom spline</a>
2. <a href="https://en.wikipedia.org/wiki/Levenberg-Marquardt_algorithm">Levenberg–Marquardt algorithm</a>
