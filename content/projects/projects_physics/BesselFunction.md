---
author: "Ying-Shan Chen"
title: "The Second Kind Bessel Function"
date: '2023-12-21'
categories: [
    "physics",
    "TA project"
]
tags: [
    "Bessel Function",
    "Numerical Integration"
]
description: "Computed Bessel functions of the second kind \\(Y_m(x)\\) using upward recursion, with starting values derived via analytical identities and numerical integration. Verified results by plotting \\(Y_m(x)\\) for various orders over the range \\(0 < x < 50\\)."
---
The second solution to Bessel's equation is \\(Y_m(x)\\), the Bessel function of the second kind. Compute the function \\(Y_m(x)\\) using upward recursion
$$
    Y_{m+1}=\frac{2m}{x}Y_m(x)-Y_{m-1}(x).
$$
To obtain the starting values for recursion, use the identities
$$
    Y_0(x) = \frac{2}{\pi} \left[ \ln{\frac{x}{2}} + \gamma \right] J_0(x) - \frac{4}{\pi} \sum^\infty_{k=1}(-1)^k \frac{J_{2k}(x)}{k}
$$
and
$$
    J_1(x)Y_0(x)-J_0(x)Y_1(x) = \frac{2}{\pi x}
$$
where \\(\gamma \approx 0.577215664\\). Demonstrate your routine by producing plots of \\(Y_m(x)\\) for \\(0 < x < 50\\) and various \\(m\\).

🔗 See more details <a href="https://github.com/ChenYingShan1114/Numerical-Integration"> here</a>.

## Numerical Integration Result
<p align="center">
    <img src="/self/img/projects_physics/BesselFunction/Bessel.png" width="700" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

