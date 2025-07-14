---
author: "Ying-Shan Chen"
title: "Finite Square Well"
date: '2023-10-30'
categories: [
    "physics",
    "TA project"
]
tags: [
    "Quantum Mechanics",
    "Numerical Simulation",
    "Solving Systems of Equations"
]
description: "This project applies Newton's method to solve the transcendental eigenvalue equations of a finite potential square well in quantum mechanics. It numerically estimates bound-state energy levels, using initial guesses derived from the infinite square well solution."
---

There are two common approaches for solving systems of equations: linear and non-linear. For linear unsteady systems, it can be solved by <a href="https://en.wikipedia.org/wiki/Gaussian_elimination"> Gaussian elimination</a> and inverse matrix. However, for nonlinear equations, <a href="https://en.wikipedia.org/wiki/Newton%27s_method">Newton's method</a> can let us approach the solution. 
This project demonstrates how Newton’s method can be applied to solve the nonlinear eigenvalue problem of a finite potential square well, where no theoritical solution exists.

## Finite Square Well
In quantum mechanics, the energy eigenvalues of finite potential square well are given by transcendental equations. Therefore, these equations are highly nonlinear and must be solved numerically or graphically. In this project, I used single-variable Newton's method to find the roots corresponding to the allowed energy eigenvalues of a bound electron in the well.

🔗 See more details <a href="https://github.com/ChenYingShan1114/Finite-Square-Well/"> here</a>.

## System conditions 
Consider an electron in a quantum square well potential of depth \\(V=-13.6 eV\\) and half-width \\(a=20a_B\\) where \\(a_B\\) is the Bohr radius.

## Energy Equations
The energy eigenvalues, \\(E>V\\), are given by the transcendental equations. For the odd states, 
$$
\sqrt{-E} = \sqrt{E-V}\tan\left(\frac{a}{\hbar}\sqrt{2m(E-V)}\right)
$$
, and the even states
$$
\sqrt{-E} = -\sqrt{E-V}\cot\left(\frac{a}{\hbar}\sqrt{2m(E-V)}\right)
$$
Since these equations cannot be solved analytically, we apply a numerical root-finding approach.

## Initial Guess
The eigenenergies of an infinite square well with the same width are
$$
E_n = \frac{n^2\pi^2 \hbar^2}{8ma^2} - 13.6.
$$
These values serve as initial guesses for the Newton iteration process.

## Simulation Result
By plotting the difference between the left- and right-hand sides of the transcendental equations, we visually identify the root locations where the plot intersects \\(y=0\\). These roots represent valid eigenenergies.
<p align="center">
    <img src="/self/img/projects_physics/FiniteSquareWell/eigenenergy.png" width="500" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>
Finally, the solutions show in the following table:
<table style="width:100%; text-align: center;">
  <thead>
    <tr style="background-color: #f0f0f0;">
      <th style="padding: 12px; border: 1px solid #ccc;">State</th>
      <th style="padding: 12px; border: 1px solid #ccc;">Initial Guess (eV)</th>
      <th style="padding: 12px; border: 1px solid #ccc;">Eigenenergy of Finite Square Well (eV)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">1</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-13.516</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-13.2954</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">2</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-13.2641</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-12.915</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">3</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-12.8442</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-12.3831</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">4</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-12.2563</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-11.7002</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">5</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-11.5004</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-10.8675</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">6</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-10.5766</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-9.88612</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">7</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-9.48483</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-8.7581</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">8</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-8.22509</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-7.4862</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">9</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-6.79738</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-6.07472</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">10</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-5.2017</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-4.53088</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">11</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-3.43806</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-2.869</td>
    </tr>
    <tr>
      <td style="padding: 12px; border: 1px solid #ccc;">12</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-1.50645</td>
      <td style="padding: 12px; border: 1px solid #ccc;">-1.12859</td>
    </tr>
  </tbody>
</table>
