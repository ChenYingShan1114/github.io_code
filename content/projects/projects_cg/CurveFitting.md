---
author: "Ying-Shan Chen"
title: "A Curve Fitting Tool"
date: '2024-05-26'
categories: [
    "computer graphics",
    "mini project"
]
tags: [
    "Computer Graphics",
    "Python"
]
description: "Implemented and compared multiple curve fitting and interpolation methods, parameterization techniques, spline continuity conditions, and subdivision algorithms for smooth curve generation and analysis."
---

By self-studing the course <a href="http://staff.ustc.edu.cn/~lgliu/Courses/GAMES102_2020/default.html">GAMES102</a>, I summarized the curve fitting methods introduced in Homework 01~05.

🔗 See more details <a href="https://github.com/ChenYingShan1114/Curve_Fitting"> here</a>.

## Curve Fitting
Implement curve fitting and interpolation using five different methods:
1. Polynomial interpolation
2. Gaussian interpolation
3. Polynomial least square
4. Polynomial ridge regression
5. Neural network

Also explored four parameterization techniques:
1. Uniform parameterization
2. Chordal parameterization
3. Centripetal parameterization
4. Foley parameterization

<p align="center">
    <img src="/self/img/projects_cg/CurveFitting/diff_fit_method.png" width="700" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
    Fix Parameterization Method
</p>
<p align="center">
    <img src="/self/img/projects_cg/CurveFitting/diff_parameterization.png" width="700" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
    Fix Fitting Method
</p>

## Cubic Splines
Solved cubic spline interpolation under various continuity constraints:
<table style="width:100%;">
    <tbody>
        <tr style="border: none; background-color:rgb(255, 255, 255);">
            <td style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/C0_continuity.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    C0 Continuity
                </p>
            </td>
            <td style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/C1_continuity.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    C1 Continuity
                </p>
            </td>
        </tr>
        <tr style="border: none; background-color:rgb(255, 255, 255);">
            <td style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/G1_continuity.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    G1 Continuity
                </p>
            </td>
            <td style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/C2_continuity.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    C2 Continuity
                </p>
            </td>
        </tr>
    </tbody>
</table>

## Subdivision
Implemented three curve subdivision methods:
<table style="width:100%;">
    <tbody>
        <tr style="border: none; background-color:rgb(255, 255, 255);">
            <td style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/Chaikin_2nd.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    Chaikin (2nd B-Spline)
                </p>
            </td>
            <td style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/Chaikin_3rd.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    Chaikin (3rd B-Spline)
                </p>
            </td>
        </tr>
        <tr style="border: none; background-color:rgb(255, 255, 255);">
            <td colspan=2 style="border: none;">
                <p align="center">
                    <img src="/self/img/projects_cg/CurveFitting/interpolation.png" width="300" style="margin-left:10px;margin-top:10px;margin-right:10px;margin-bottom:10px"> <br>
                    4 points interpolation
                </p>
            </td>
        </tr>
    </tbody>
</table>