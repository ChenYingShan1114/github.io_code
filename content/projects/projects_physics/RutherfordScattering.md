---
author: "Ying-Shan Chen"
title: "Rutherford Scattering"
date: '2023-10-14'
categories: [
    "physics",
    "TA project"
]
tags: [
    "Classical Mechanics",
    "Numerical Simulation",
    "Ordinary Differential Equation"
]
description: "A numerical simulation of Rutherford scattering using the adaptive Runge-Kutta method to model the Coulomb interaction between an alpha particle and a gold nucleus."
---
In <a href="https://en.wikipedia.org/wiki/Rutherford_scattering_experiments#Rutherford_scattering"> Rutherford’s historic experiment </a>, alpha particles were observed to scatter when passing near the gold nuclei in a thin foil. This experiment disproved the <a href="https://en.wikipedia.org/wiki/Plum_pudding_model"> plum pudding model </a> and provided strong evidence for the existence of a small, dense atomic nucleus.

In this project, I recreated the scattering process using a numerical simulation of the Coulomb force between an alpha particle and a gold ion. The simulation is solved using the adaptive Runge-Kutta method, which provides high accuracy when modeling the particle’s trajectory under the influence of electrostatic repulsion.

To verify the correctness of the simulation, I compared the results with the analytical theoretical solution for Rutherford scattering, showing good agreement between the two.

🔗 See more details <a href="https://github.com/ChenYingShan1114/Rutherford-Scattering"> here</a>.

## Governing equations 

Rutherford scattering describes the deflection of a charged particle (such as an alpha particle) due to the Coulomb force exerted by a heavy nucleus (such as gold). The equation of motion for the alpha particle is given by:
$$
\vec{F}=\frac{q_{\alpha}q_{Au}}{4\pi \epsilon_0} \frac{\vec{r}}{|r^3|}=m_{\alpha}\frac{d\vec{v}}{dt}.
$$

Here: <br>
• \\(q_\alpha\\) and \\(q_{Au}\\) are the charges of the alpha particle and the gold nucleus, respectively, <br>
• \\(\vec{v}\\) is the displacement vector from the gold nucleus to the alpha particle,<br>
• \\(m_\alpha\\) is the mass of the alpha particle, and<br>
• \\(\epsilon_0\\) is the vacuum permittivity.


Since the simulation involves motion at the atomic scale, applying appropriate normalization and unit conversion improves numerical stability and accuracy.

## Theoritical solution 

The theoretical solution of Rutherford scattering is $$\tan{\frac{\varphi}{2}}=\frac{p_0}{2p},$$
where <br>
• \\(\varphi\\) is the scattering angle,<br>
• \\(p\\) is the impact parameter (the perpendicular distance from the initial trajectory to the center of force),<br>
• \\(p_0\\) value corresponds to the distance at which all kinetic energy is converted into electrostatic potential energy
$$p_0=\frac{1}{4\pi\epsilon_0}\frac{2qq_0}{mv_0^2}.$$ 
<p align="center">
    <img src="/self/img/projects_physics/RutherfordScattering/Rutherford_scattering.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

## Simulation Result 
<p align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/F-IbTDQFSSQ?si=8u1IsgeSpBRBURyM&autoplay=1&loop=1&playlist=F-IbTDQFSSQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>
Numerical trajectory of alpha particle using adaptive Runge-Kutta method
<p align="center">
    <img src="/self/img/projects_physics/RutherfordScattering/Rutherford_scattering_RK4.png" width="600" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>