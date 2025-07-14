---
author: "Ying-Shan Chen"
title: "Pancake Simulation"
date: '2025-05-28'
categories: [
    "computer graphics",
    "work project"
]
tags: [
    "Computer Graphics",
    "Physics Engine",
    "NVIDIA Omniverse"
]
resume: "Built physics-based animation of pancake cooking in NVIDIA Omniverse Isaac Sim using fluid and deformable body simulation. Tuned physical parameters to generate realistic motion and created AI training data for real-world robotic arm manipulation."

description: "Simulated pancake-cooking scenes using NVIDIA Omniverse Isaac Sim and PhysX, with the goal of training a real-world robotic arm for cooking tasks. By carefully adjusting material properties and separating batter and pancake states across two physics scenes, we achieved realistic deformation and fluid dynamics for animation data generation."
---
Our final goal is to use a robotic arm to control a spatula and implement an autonomous cooking robot. To achieve this, NVIDIA Omniverse is a good tool to generate diverse video simulations, which are used to train a robotic arm's motion for real-world deployment.

In this project, I use Isaac Sim as the physics engine to simulate the process of cooking a pancake. By tuning physical parameters of the batter and pancake, I created a realistic animation that mimics real-world pancake cooking behavior in a kitchen setting.

## Object Settings
<p align="center">
    <table style="width:100%;">
        <thead>
            <tr style="background-color: #f0f0f0;">
                <th>Object</th>
                <th>Source</th>
                <th>Collider</th>
                <th>Physics Property</th>
                <th>Material</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td align="center">Pan</td>
                <td align="center" rowspan=3>3DGS to Mesh Grid</td>
                <td align="center">Yes</td>
                <td align="center">-</td>
                <td align="center">-</td>
            </tr>
            <tr>
                <td align="center">Spatula</td>
                <td align="center">Yes</td>
                <td align="center">Rigid Body</td>
                <td align="center">-</td>
            </tr>
            <tr>
                <td align="center">Container</td>
                <td align="center">Yes</td>
                <td align="center">-</td>
                <td align="center">-</td>
            </tr>
            <tr>
                <td align="center">Batter</td>
                <td align="center" rowspan=2 style="background-color:rgb(255, 255, 255);">Mesh Grid</td>
                <td align="center">No</td>
                <td align="center">Particle Sampler with Isosurface</td>
                <td align="center">PBD Particle</td>
            </tr>
            <tr>
                <td align="center">Pancake</td>
                <td align="center">No</td>
                <td align="center">Deformable Body</td>
                <td align="center">Deformable Body</td>
            </tr>
        </tbody>
    </table>
</p>

## Physics Scene Configuration
Because the state of batter and pancake can't transfor like the real world work, I use two separate physics scenes — one for the batter and one for the cooked pancake — because physics interactions in Omniverse occur even if an object is invisible. Separating them ensures clean transitions and prevents unwanted interactions.
1. Scene 1: container, batter, pan
2. Scene 2: spatula, pancake, pan

## Adjusting Physical Parameters
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/RM-HoD7I5DE?si=lBosfyzhkJ9i6syk&autoplay=1&loop=1&playlist=RM-HoD7I5DE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>
<p align="center">
    <table style="width:70%;">
        <thead>
            <tr style="background-color: #f0f0f0;">
                <th>Fluid Parameter</th>
                <th>Left</th>
                <th>Middle</th>
                <th>Right</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td align="center">density</td>
                <td align="center">1.0</td>
                <td align="center">10.0</td>
                <td align="center">0.0</td>
            </tr>
            <tr>
                <td align="center">fiction</td>
                <td align="center">0.0</td>
                <td align="center">0.2</td>
                <td align="center">0.2</td>
            </tr>
            <tr>
                <td align="center">surface tension</td>
                <td align="center">0.0</td>
                <td align="center">0.5</td>
                <td align="center">0.0</td>
            </tr>
            <tr>
                <td align="center">viscosity</td>
                <td align="center">0.0</td>
                <td align="center">50.0</td>
                <td align="center">50000.0</td>
            </tr>
            <tr>
                <td align="center">cohesion</td>
                <td colspan=3 align="center">0.0</td>
            </tr>
            <tr>
                <td align="center">damping</td>
                <td colspan=3 align="center">0.0</td>
            </tr>
            <tr>
                <td align="center">drag</td>
                <td colspan=3 align="center">0.0</td>
            </tr>
            <tr>
                <td align="center">lift</td>
                <td colspan=3 align="center">0.0</td>
            </tr>
        </tbody>
    </table>
</p>

## Final Physical Parameters
Most parameters are set as defualt, except
<p align="center">
    <table style="width:100%;">
        <thead>
            <tr style="background-color: #f0f0f0;">
                <th>Object</th>
                <th>Parameters</th>
                <th>Value</th>
                <th>Unit</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td align="center" rowspan=4>Pancake (Mesh)</td>
                <td align="center">mass</td>
                <td align="center">0.2</td>
                <td align="center">kg</td>
            </tr>
            <tr>
                <td align="center">simulation mesh resolution</td>
                <td align="center">5</td>
                <td align="center">-</td>
            </tr>
            <tr>
                <td align="center">vertex velocity damping</td>
                <td align="center">10</td>
                <td align="center">1/s</td>
            </tr>
            <tr>
                <td align="center">rest offset</td>
                <td align="center">0</td>
                <td align="center">m</td>
            </tr>
            <tr>
                <td align="center" rowspan=2>Pancake (Material)</td>
                <td align="center">dynamic fiction</td>
                <td align="center">0.5</td>
                <td align="center">-</td>
            </tr>
            <tr>
                <td align="center">Young's modulus</td>
                <td align="center">50000</td>
                <td align="center">kg/m/s<sup>2</sup>=N/m<sup>2</sup></td>
            </tr>
            <tr>
                <td align="center">Batter (Particle System)</td>
                <td align="center">particle contact offset</td>
                <td align="center">0.005</td>
                <td align="center">m</td>
            </tr>
            <tr>
                <td align="center" rowspan=3 style="background-color:rgb(255, 255, 255);">Pancake (Material)</td>
                <td align="center">density</td>
                <td align="center">10</td>
                <td align="center">kg/m<sup>3</sup></td>
            </tr>
            <tr>
                <td align="center">surface tension</td>
                <td align="center">0.5</td>
                <td align="center">1/m<sup>3</sup></td>
            </tr>
            <tr>
                <td align="center">viscosity</td>
                <td align="center">50</td>
                <td align="center">-</td>
            </tr>
        </tbody>
    </table>
</p>
<!--
Parameter Descriptions:
• simulation mesh resolution: use how mant mesh to simulate the motion of deformable body. Bigger the value, softer the object.
• vertex velocity damping: provide a drag force to vertices on mesh, act like air drag. Bigger the value, stiffer the object.
• rest offset: the rest offset of rigid body.
• Young's modulus: the stiffness of material. Smaller the value, softer the object.
• particle contact offset: the distance between particles. Smaller the value, smaller the distance between particles, therefore there will have more particles under same volume and cost more computational resource.
• viscosity: how sticky the fluid is.
-->

## Simulation Result
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jRciGPLgf7U?si=vZgFnR9-Ms2Aqlow&autoplay=1&loop=1&playlist=jRciGPLgf7U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>