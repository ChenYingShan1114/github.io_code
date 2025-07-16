---
author: "Ying-Shan Chen"
title: "3DGS Rrefrigerator Animation"
date: '2025-02-21'
categories: [
    "computer graphics",
    "intern project"
]
tags: [
    "Computer Graphics",
    "3D Gaussian Splat",
    "Java Script"
]
resume: "Generated 3D Gaussian Splatting models from multi-view object capture and implemented interactive animations using Three.js for real-to-sim visualization"

description: "Captured real-world objects to generate 3D Gaussian Splatting (3DGS) models and created interactive scenes with animations using Three.js."
---
## 3D Gaussian Splat Model

During my internship at ITRI, I worked on capturing multi-view images of physical objects to generate <a href="https://github.com/MrNeRF/awesome-3D-gaussian-splatting?tab=readme-ov-file#seminal-paper-introducing-3d-gaussian-splatting">3D Gaussian Splatting (3DGS)</a> models. After taking photos from various angles, the images were processed into .ply files using our in-house pipeline. Unlike traditional point clouds, these models use anisotropic Gaussians with spherical harmonic shading, allowing them to reflect color and detail based on viewing direction.

Higher-order spherical harmonics result in more vivid, accurate models—but also require more storage. This technique excels at capturing surface details such as scratches, engravings, and textures, but has limitations when handling transparent, reflective, symmetric, or low-contrast objects due to challenges in feature detection.

Personally, I find 3DGS a meaningful way to digitally preserve sentimental items without taking up physical space. Below are two examples I reconstructed:

1. Slinky Dog, which is my favorite Pixar character. I purchased at Tokyo Disneyland.
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/WyFcS6JCUUA?si=-PTVyFrgMxis6-VZ&autoplay=1&loop=1&playlist=WyFcS6JCUUA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

2. Einstein doll, which my dad bought for me when he traveled to Europe, symbolizing our shared physics background.
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/A7ipDpDIhX8?si=AAKfSAixf4cqVkL2&autoplay=1&loop=1&playlist=A7ipDpDIhX8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

## 3DGS Animation
🔗 See more details <a href="https://github.com/ChenYingShan1114/Fridge-Animation"> here</a>.

To explore real-to-sim animation, I created an animated demo of a fridge model reconstructed using 3DGS:
1. A 3DGS fridge model (with open door) was provided by a teammate.
2. Using <a href="https://superspl.at/editor/"> SuperSplat</a> as editor, I segmented the fridge door and adjusted both fridge body and door models' pivot axis to the closest principle axis for animation.\
⚠️ Note: Avoid large model rotations since spherical harmonics don’t rotate with the geometry.
3. I implemented the animation using Three.js, rotating the door to simulate an opening sequence.

<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jVAnlvHCA4E?si=v34I36xKSirCQY-T&autoplay=1&loop=1&playlist=jVAnlvHCA4E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

## Final Scene
To complete the simulation, I placed the fridge in a virtual room and added interactable elements such as a cake inside the fridge or on a table.
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/EEthVJPCRZo?si=xPuSPmrN77rIC-sx&autoplay=1&loop=1&playlist=EEthVJPCRZo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>