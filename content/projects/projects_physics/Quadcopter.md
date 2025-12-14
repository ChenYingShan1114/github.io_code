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

<span style="display: flex; flex-direction: column; align-items: center; height: 700px;">
    <br>
    <div style="font-size: 18px;">Quadcopter Simulation</div>
    <div id="threejs-container-quadcopter" style="width: 700px; height: 600px;"><div class = 'moveGUI-quadcopter' style="position: absolute; "></div></div>     
</span>

<script type="module" src="/self/js/threejs_script_quadcopter.js"></script>
</main>