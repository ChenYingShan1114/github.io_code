---
author: "Ying-Shan Chen"
title: "Acceptance-Rejection Distribution Generator"
date: '2023-12-14'
categories: [
    "TA project"
]
tags: [
    "Random Number",
    "Stochastic Method"
]
description: "Used the acceptance-rejection method to generate samples from custom continuous and discrete distributions, including binomial and Poisson. Verified accuracy through histogram comparisons with analytical formulas."
---
## Acceptane-Rejection Sampling Method
Acceptance-rejection is a technique for building generators of distributions, which works well both on continuous and discrete random variables. The general idea is analogous to throwing darts at a dartboard.
Consider a continuous random variable \\(x\\) distributed in \\([a,b)\\) with a proba-
bility distribution \\(P_x(x)\\). We select a value \\(P^{max}_x(x)\\) with the condition

$$
    P^{max}_x \ge P_x(x)
$$

for all \\(x\\). There are four steps that the scheme selecting a random value for \\(x\\):

1. Generate a trial value \\(x_{try} = a + (b-a)R_1\\), where \\(R_1\\) is a uniform random number between \\(0\\) and \\(1\\).
2. Compute the probability density at the trial point \\(P(x_{try})\\).
3. Accept \\(x_{try}\\) as the generated random number if 
$$
    \frac{P(x_{try})}{P^{max}_x} \ge R_2
$$
where \\(R_2\\) is another independent uniform number.
4. If this condition is not satisfied, \\(x_{try}\\) is rejected, and we return to step 1 and try again.

<p align="center">
    <img src="/self/img/projects_physics/DistributionGenerator/acceptance-rejection-method.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

The figure shows a geometric interpretation of this scheme. Picture a rectangle bounded by \\(x=[a,b)\\) and \\(y=[0,P_x^{max})\\). We select a random point \\((x_{try}, y_{try})\\) inside this rectangle, where \\(y_{try}=P^{max}_x R_2\\). If this point lands in the shaded region, below the curve \\(P_x(x)\\), then it is accepted. The larger the rejection scheme is exact if \\(P^{max}_x\\) satisfies \\(P^{max}_x \ge P_x(x)\\). However, it is most efficient when \\(P^{max}_x = max(P_x(x))\\), since this minimizes the number of rejections. 

This method also extends easily to discrete distributions. We can simply replace the curve with a histogram.


🔗 See more details <a href="https://github.com/ChenYingShan1114/Distribution-Generator"> here</a>.

## Examples
Test the method by generating \\(10^6\\) samples using the acceptance-rejection method. The left plot shows the accepted sampling points. The right histogram confirms good agreement with the target distribution.
1. Use acceptance-rejection to generate the distribution 
$$
    P_x(x)dx = \frac{3}{4}(1-x^2)dx
$$
where \\(-1 \le x \le 1 \\).
<p align="center">
    <img src="/self/img/projects_physics/DistributionGenerator/acceptance-rejection.png" width="700" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

2. Use binomial distribution 
$$
    P_k[k]=\frac{N!}{k!(N-k)!} \left(\frac{1}{2}\right)^2
$$
where \\(k=0,...,N\\).
<p align="center">
    <img src="/self/img/projects_physics/DistributionGenerator/binomial-distribution.png" width="700" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>

3 Use Poisson distribution
$$
    P_i[i]=\frac{e^{-\lambda} \lambda^i}{i!}
$$
where \\( 0 \le i \le \infty \\) and \\(\lambda=10\\).
<p align="center">
    <img src="/self/img/projects_physics/DistributionGenerator/poisson-distribution.png" width="700" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> 
</p>