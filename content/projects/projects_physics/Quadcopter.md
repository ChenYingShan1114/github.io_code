---
author: "Ying-Shan Chen"
title: "Quadcopter"
date: '2025-08-14'
categories: [
    "Physics",
    "Work Project"
]
tags: [
    "NVIDIA Omniverse",
    "Classical Mechanics",
    "Numerical Simulation",
    "Derivation",
    "Java Script",
    "three.js"
]
resume: "Developed a physics-based quadcopter simulation by deriving its equations of motion and integrating the model into NVIDIA Omniverse using Kit Extension tools."

description: "Derivative the eqaution of motion of quadcopter and implement the motion by an interactive scene."
---
<main>

<p align="center" >
    <iframe class="pdf" view="fit" src="/self/pdf/projects_physics/Quadcopter/20250822.pdf" width="600" height="500"> </iframe>
</p>

## Play the Quadcopter Here!
<span style="display: flex; flex-direction: column; align-items: center; height: 500px;">
    <!-- <br> -->
    <!-- <div style="font-size: 18px;">Quadcopter Simulation</div> -->
    <div id="threejs-container-quadcopter" style="width: 700px; height: 500px;"><div class = 'moveGUI-quadcopter' style="position: absolute; "></div></div>     
</span>

## Demo Video on Omniverse Platform
<p align="center">
    <video src="/self/mp4/projects_physics/Quadcopter/quadcopter_1.mp4" autoplay controls loop type="video/mp4" width="650"></video>
    <video src="/self/mp4/projects_physics/Quadcopter/quadcopter_2.mp4" autoplay controls loop type="video/mp4" width="650"></video>
</p>

<script type="module" src="/self/js/threejs_script_quadcopter.js"></script>
</main>