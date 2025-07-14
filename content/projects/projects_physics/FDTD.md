---
author: "Ying-Shan Chen"
title: "One-Dimensional Simulation with the FDTD Method"
date: '2020-10-20'
categories: [
    "physics",
    "research project"
]
tags: [
    "Finite-Difference Time-Domain method",
    "electromagnetic",
    "Python"
]
description: "Simulated electromagnetic wave propagation using FDTD in vacuum, dielectric, and lossy dielectric media with hard, soft, and absorbing boundary conditions."
---

<p align="center" >
    <iframe class="pdf" src="/self/pdf/projects_physics/FDTD/fdtd1.pdf" width="600" height="500"> </iframe>
</p>

## Boundary Condition
1. Fixed boundary condition with hard source
<p align="center">
    <img src="/self/gif/projects_physics/FDTD/fdtd_1_ex_fixed_hard.gif" width="500">
    <img src="/self/gif/projects_physics/FDTD/fdtd_1_hy_fixed_hard.gif" width="500">
</p>

2. Fixed boundary condition with soft source
<p align="center">
    <img src="/self/gif/projects_physics/FDTD/fdtd_1_ex_fixed_soft.gif" width="500">
    <img src="/self/gif/projects_physics/FDTD/fdtd_1_hy_fixed_soft.gif" width="500">
</p>

3. Absorb boundary condition
<p align="center">
    <iframe class="pdf" src="/self/pdf/projects_physics/FDTD/fdtd2.pdf" width="600" height="500"> </iframe>
</p>
<p align="center">
    <img src="/self/gif/projects_physics/FDTD/fdtd_2_ex.gif" width="500">
    <img src="/self/gif/projects_physics/FDTD/fdtd_2_hy.gif" width="500">
</p>

## Propagation in Medium
1. Dielectric Medium
<p align="center">
    <iframe class="pdf" src="/self/pdf/projects_physics/FDTD/fdtd3.pdf" width="600" height="460"> </iframe>
</p>

The reflection coefficient is
$$
    \varGamma = \frac{\sqrt{\epsilon_0} - \sqrt{\epsilon_r}}{\sqrt{\epsilon_0} + \sqrt{\epsilon_r}}
$$
and the transmission coefficient is
$$
    \tau = \frac{2\sqrt{\epsilon_0}}{(\sqrt{\epsilon_0} + \sqrt{\epsilon_r})}.
$$
The region where \\(x > 100\\) has a relative permittivity \\(\epsilon_r\\) of 4.

<p align="center">
    <img src="/self/gif/projects_physics/FDTD/fdtd_3_ex.gif" width="500">
    <img src="/self/gif/projects_physics/FDTD/fdtd_3_hy.gif" width="500">
</p>

2. Lossy Dielectric Medium
<p align="center">
    <iframe class="pdf" src="/self/pdf/projects_physics/FDTD/fdtd4.pdf" width="600" height="460"> </iframe>
</p>

The region where \\(x > 100 \\) has a relative permittivity \\(\epsilon_r = 4\\) and electrical conductivity \\(\sigma = 0.04\\).

Otherwise, the theoretical decay rate in a lossy dielectric medium is given by
$$
    \alpha = \frac{\omega}{c_0} \sqrt{\frac{\epsilon_r}{2}} \left[\sqrt{1+\left(\frac{\sigma}{\omega \epsilon_0 \epsilon_r} \right)^2} -1 \right]^{\frac{1}{2}}.
$$
<p align="center">
    <img src="/self/gif/projects_physics/FDTD/fdtd_5_ex.gif" width="500">
    <img src="/self/gif/projects_physics/FDTD/fdtd_5_hy.gif" width="500">
</p>