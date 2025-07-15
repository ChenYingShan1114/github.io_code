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
resume: "Using the model to build 3D Gaussian splat point clouds by taking lots of pictures for an object."

description: "....."
---
## 3D Gaussian Splat Model
At the beginning I started to work as intern in ITRI, my main job is taking picture for an object from different directions. The pictures should cover as many views from different direction as possible. After input the pictures as data into the program which the software engineer in our group already built, it will generate a .ply file which is like a point cloud model. However, those are not only points. They are <a href="https://github.com/MrNeRF/awesome-3D-gaussian-splatting?tab=readme-ov-file#seminal-paper-introducing-3d-gaussian-splatting"> Gaussian Splat </a>which have different color when audieunce see them from different direction. The higher the spherical harmonic order, the colorful the Gaussian splat, the more accuracy of the object model, the large the data storage need.

It is a good technique that it can reconstruct the details on model, such like scratches or words. But it is hard to rebuild some transparent material, such like glass or acrylic sheet, or highly reflective material, such like iron. Also, highly symmetric model or dark color model are hard to find feature points. So it is also hard to rebuild. The following are two dolls that I reconstructed by this technique and it provides me a good way to keep some important memories without any physical space storage.

1. Slinky Dog, which is my favorite character in Pixar movies. It is a doll bought from Tokyo Disney Land.
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/WyFcS6JCUUA?si=-PTVyFrgMxis6-VZ&autoplay=1&loop=1&playlist=WyFcS6JCUUA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

2. Einstein doll, which my dad bought for me when he travel to Europe, because I am a physics major student and he is a professor in department of physics.
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/A7ipDpDIhX8?si=AAKfSAixf4cqVkL2&autoplay=1&loop=1&playlist=A7ipDpDIhX8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

## Animation on 3D Gaussian Splat
🔗 See more details <a href="https://github.com/ChenYingShan1114/Fridge-Animation"> here</a>.

Next, I try to make the animation of 3DGS file in order to demo some real-to-sim technique. 
1. My coworker generate a refrigerator with upper door opened. 
2. I use <a href="https://superspl.at/editor/"> supersplat</a> as editor to split fridge's door and body into two models. Also, turn the rotational axis to the closest x, y, z axis in order to rotate fridge's door easily when making animation.
Notice: Do not rotate the model too much because the spherical harmonic which represent different color watch from different direction on each point can't rotate with the model.
3. I use three.js to make an animation, shown in following:

<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jVAnlvHCA4E?si=v34I36xKSirCQY-T&autoplay=1&loop=1&playlist=jVAnlvHCA4E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

## Simulation Result
Finally, I add a scene behind the fridge. Also, I can put a cake inside the fridge or on the table.
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jRciGPLgf7U?si=vZgFnR9-Ms2Aqlow&autoplay=1&loop=1&playlist=jRciGPLgf7U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>