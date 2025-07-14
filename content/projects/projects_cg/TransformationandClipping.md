---
author: "Ying-Shan Chen"
title: "Transformation and Clipping"
date: '2022-10-31'
categories: [
    "computer graphics",
    "course project"
]
tags: [
    "Computer Graphics",
    "OpenGLUT",
    "C++"
]
description: "Implemented a 2D graphics interpreter that reads and executes transformation commands (translate, scale, rotate), clipping, and viewport mapping from input files. Supports drawing squares and triangles with random colors and visualizes the result using view transformation."
---

There are many test data in the forder and many input commands in each test data. 
I read the files and complete the following instructions. Also, each shape will automatically be assigned a random color.

🔗 See more details <a href="https://github.com/ChenYingShan1114/Transformation_and_Clipping"> here</a>.

## Operating instructions
* ### Comment:
    The instruction is `# ......`<br>
    If a `#` appears, skip the line. (i.e. You don't need to execute the line which # appears.)  
    
* ### Reset:
    The instruction is `reset`<br>
    Reset the transformation matrix.
    
* ### Translate:
    The instruction is `translate x y`<br>
    `x` means moving along x-axis by `x` unit.<br>
    `y` means moving along y-axis by `y` unit.

* ### Scale:
    The instruction is `scale x y`<br>
    `x` means scaling along x-axis by `x` unit.<br>
    `y` means scaling along y-axis by `y` unit.
    
* ### Rotate:
    The instruction is `rotate θ`<br>
    `θ` means rotating along z-axis by θ degree.

* ### Clear data:
    The instruction is `clearData`<br>
    Clear the objects that you create (square and triangle).

* ### Clear screen:
    The instruction is `clearScreen`<br>
    Clear the screen.

* ### View:
    The instruction is `view wxl wxr wyb wyt vxl vxr vyb vyt`<br>
    `wxl wxr wyb wyt` means the position of object before mapping.<br>
    `vxl vxr vyb vyt` means the position of object after mapping.<br>
    
    In math words <br>

        f(wxl,wyb) = (vxl,vyb)
        f(wxr,wyt) = (vxr,vyt)
    where it is a linear transformation.<br>
    The objects outside the boundary need to **clipped**.<br>
    Every time you execute `view`, the created objects must be displayed. Please draw the boundary of objects with points and lines.(Use the code in lab1)
    Please add `system("pause");` when you display anything.

* ### Square:
    The instruction is `square`<br>
    Create a square with its vertex `(-1,-1)` `(1,-1)` `(1,1)` `(-1,1)`.

* ### Triangle:
    The instruction is `triangle`<br>
    Create a triangle with its vertex `(0,1)` `(-1,-1)` `(1,-1)`.

* ### End:
    The instruction is `end`<br>
    Destory the window.
  
## Results
    
1. 
<p align="center">
    <img src="/self/img/projects_cg/TransformationandClipping/lab2A-1.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/TransformationandClipping/lab2A-2.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/TransformationandClipping/lab2A-3.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

2. 
<p align="center">
    <img src="/self/img/projects_cg/TransformationandClipping/lab2B.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

3. 
<p align="center">
    <img src="/self/img/projects_cg/TransformationandClipping/lab2C.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

4. 
<p align="center">
    <img src="/self/img/projects_cg/TransformationandClipping/lab2D.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

5. 
<p align="center">
    <img src="/self/img/projects_cg/TransformationandClipping/lab2E-1.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/TransformationandClipping/lab2E-2.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/TransformationandClipping/lab2E-3.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

