---
author: "Ying-Shan Chen"
title: "Finite Element Method"
date: '2026-02-12'
categories: [
    "Computer Graphics",
    "Practice"
]
tags: [
    "Physical Based Animation",
    "variational principle",
    "C++"
]
description: "Use finite element method to implement deformable objects."
---

🔗 See more details about <a href="https://github.com/ChenYingShan1114/finite-element-method">finite element method</a>, forked from the projects in physical-based animation course at University of Toronto.

Using neo-Hookean strain energy function.
  
## Linearly Implicit Euler Method
    
* ### Stanford Bunny
    * ### Coarse Tetrahedral Grid

    <p align="center">
        <video src="/self/mp4/projects_cg/FiniteElementMethod/fem-linearly-bunny.mov" controls type="video/mov" width="600"></video>
    </p>

    * ### Coarse Tetrahedral Grid with High Poly Skinning

    <p align="center">
        <video src="/self/mp4/projects_cg/FiniteElementMethod/fem-linearly-bunny-skinning.mov" controls type="video/mov" width="600"></video>
    </p>

* ### Armadillo
    * ### Coarse Tetrahedral Grid

    <p align="center">
        <video src="/self/mp4/projects_cg/FiniteElementMethod/fem-linearly-arma.mov" controls type="video/mov" width="600"></video>
    </p>

    * ### Coarse Tetrahedral Grid with High Poly Skinning
    <p align="center">
        <video src="/self/mp4/projects_cg/FiniteElementMethod/fem-linearly-arma-skinning.mov" controls type="video/mov" width="600"></video>
    </p>



## Fully Implicit with Newton Method
* ### Armadillo
    * ### Coarse Tetrahedral Grid

    <p align="center">
        <video src="/self/mp4/projects_cg/FiniteElementMethod/fem-newton-arma.mov" controls type="video/mov" width="600"></video>
    </p>
<!-- * ### Cube
<p align="center">
    <video src="/self/mp4/projects_cg/MassSpringSystem/3d-mass-spring-cube.mov" controls type="video/mov" width="600"></video>
</p>

* ### Cylinder
<p align="center">
    <video src="/self/mp4/projects_cg/MassSpringSystem/3d-mass-spring-cylinder.mov" controls type="video/mov" width="600"></video>
</p>

* ### Stanford Bunny
<p align="center">
    <video src="/self/mp4/projects_cg/MassSpringSystem/3d-mass-spring-bunny.mov" controls type="video/mov" width="600"></video>
</p> -->

## Reference
1. <a href="https://www.youtube.com/watch?v=ngaYNdNtbec&list=PLTkE7n2CwG_PH09_q0Q7ttjqE2F9yGeM3&index=6">Physics-based animation lecture 4: The Finite Element Method
</a>
2. <a href="https://www.youtube.com/watch?v=wpZe1PI7uhQ&list=PLTkE7n2CwG_PH09_q0Q7ttjqE2F9yGeM3&index=3">Physics-based animation lecture 5: OH NO! It's More Finite Elements</a>
3. <a href="https://en.wikipedia.org/wiki/Neo-Hookean_solid">Neo-Hookean solid</a>
4. <a href="https://gemini.google.com/share/972decb052d2">Gemini Note</a>