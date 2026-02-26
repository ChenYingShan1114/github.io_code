---
author: "Ying-Shan Chen"
title: "Cloth Simulation"
date: '2026-02-26'
categories: [
    "Computer Graphics",
    "Practice"
]
tags: [
    "Physical Based Animation",
    "variational principle",
    "Finite Element Method",
    "C++"
]
description: "Use finite element (triangle) method to implement membrane object simulation with basic collision detection."
---

🔗 See more details about <a href="https://github.com/ChenYingShan1114/cloth-simulation">cloth simulation</a>, forked from the projects in physical-based animation course at University of Toronto.

Using co-rotational linear elasticity energy model.
  
## Linearly Implicit Euler Method
<p align="center">
    <video src="/self/mp4/projects_cg/ClothSimulation/cloth-linearly.mov" controls type="video/mov" width="600"></video>
</p>    

* ### With Collistion
<p align="center">
    <video src="/self/mp4/projects_cg/ClothSimulation/cloth-linearly-collision.mov" controls type="video/mov" width="600"></video>
</p>    


## Fully Implicit with Gradient Descent
<p align="center">
    <video src="/self/mp4/projects_cg/ClothSimulation/cloth-gradient_descent.mov" controls type="video/mov" width="600"></video>
</p>    



## Fully Implicit with Newton Method
<p align="center">
    <video src="/self/mp4/projects_cg/ClothSimulation/cloth-newton.mov" controls type="video/mov" width="600"></video>
</p>    


## Reference
1. <a href="https://www.youtube.com/watch?v=MJj17gpmrI4&list=PLTkE7n2CwG_PH09_q0Q7ttjqE2F9yGeM3&index=8">Physics-based animation lecture 6: Cloth Simulation</a>
2. <a href="https://gemini.google.com/app/6d549414b840ab0d">Gemini Note</a>