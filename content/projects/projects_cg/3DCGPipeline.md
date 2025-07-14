---
author: "Ying-Shan Chen"
title: "3D Computer Graphics Pipeline"
date: '2022-11-28'
categories: [
    "computer graphics",
    "course project"
]
tags: [
    "Computer Graphics",
    "OpenGLUT",
    "C++"
]
description: "Implemented a 3D graphics pipeline that reads transformation, camera, and display commands from input files. Supports translation, scaling, rotation, clipping, viewport mapping, and .obj model rendering with back-face culling and triangle slicing."
---

There are many test data in the forder and many input commands in each test data. 
I read the files and complete the following instructions. Otherwise, the program would delete the graphic that is backward from camera.

🔗 See more details <a href="https://github.com/ChenYingShan1114/3D_CG_Pipeline"> here</a>.

## Operating instructions
* ### Head:
    The instruction is `Width Height`<br>
    In the head of the files will give 2 integrals that represent the windows' width and height respectively.

* ### Comment:
    The instruction is `# ......`<br>
    If `#` appears, skip the line. (i.e. You don't need to execute the line which `#` appears.)  
   
* ### Reset:
    The instruction is `reset`<br>
    Reset the transformation matrix.
   
* ### Translate:
    The instruction is `translate x y z`<br>
    `x` means moving along x-axis by `x` unit.<br>
    `y` means moving along y-axis by `y` unit.<br>
    `z` means moving along z-axis by `z` unit.

* ### Scale:
    The instruction is `scale x y z`<br>
    `x` means scaling along x-axis by `x` unit.<br>
    `y` means scaling along y-axis by `y` unit.<br>
    `z` means scaling along z-axis by `z` unit.
   
* ### Rotate:
    The instruction is `rotate x y z`<br>
    `x` means rotating along x-axis by `x` degree.<br>
    `y` means rotating along y-axis by `y` degree.<br>
    `z` means rotating along z-axis by `z` degree.<br>
    **The rotating part should be implement in the order of y-axis -> z-axis -> x-axis.**

* ### Clear data:
    The instruction is `clearData`<br>
    Clear the objects that you read from .obj file.

* ### Clear screen:
    The instruction is `clearScreen`<br>
    Clear the screen.

* ### Observe:
    The instruction is `observe epx epy epz COIx COIy COIz Tilt Hither Yon Hav`<br>
    Set the camera's parameter:<br>
    1. `epx epy epz` are the `x y z` position of the camera.<br>
    2. `COIx COIy COIz` are the point that the camera look at.<br>
   
    ```
    forward = COI - ep
    ```
    3. `Tilt` is the angle that the camera tilt.<br>
    4. `Hither Yon` are the `near` plane position and `far` plane position.<br>
    5. `Hav` is field of view.
   
* ### Viewport:
    The instruction is `view vxl vxr vyb vyt`<br>
    Since the perspective divide, all graphic will lies in `[-1, 1] X [-1, 1]`.<br>
    `-1 1 -1 1` means the left, right, botton, top boundary after perspective divide.<br>
    `vxl vxr vyb vyt` means the left, right, botton, top boundary of viewport after perspective divide.<br>

    In math words <br>

        f(-1, 1) = (0, Width)
        f(-1, 1) = (0, Height)
    where it is a linear transformation.<br>
    The objects outside the viewport boundary need to *clipped*.<br>
    Need to display the graphic in `display`.

* ### Object:
    The instruction is `object **.obj`<br>
    The `**.obj` means the name of the files. Please load the document into your code and also slice square into triangles.

* ### Display:
    The instruction is `display`<br>
    Do the `clearScreen` when display is occured.<br>
    Draw the boundary of objects with points and lines.<br>
    Add `fgetc(stdin);` when display.
   
* ### End:
    The instruction is `end`<br>
    Destory the window.
  
## Results
    
1. 
<p align="center">
    <img src="/self/img/projects_cg/3DCGPipeline/lab3A-1.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/3DCGPipeline/lab3A-2.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

2. 
<p align="center">
    <img src="/self/img/projects_cg/3DCGPipeline/lab3B-1.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/3DCGPipeline/lab3B-2.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/3DCGPipeline/lab3B-3.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

3. 
<p align="center">
    <img src="/self/img/projects_cg/3DCGPipeline/lab3C-1.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/3DCGPipeline/lab3C-2.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

4. 
<p align="center">
    <img src="/self/img/projects_cg/3DCGPipeline/lab3D.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

5. 
<p align="center">
    <img src="/self/img/projects_cg/3DCGPipeline/lab3E-1.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
    <img src="/self/img/projects_cg/3DCGPipeline/lab3E-2.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

