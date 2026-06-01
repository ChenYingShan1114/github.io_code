---
author: "Ying-Shan Chen"
title: "Digital Earth"
date: '2026-02-15'
categories: [
    "Computer Graphics",
    "Work Project"
]
tags: [
    "NVIDIA Omniverse",
    "Python"
]
# resume: "Developed weathers visual effects in NVIDIA Omniverse using Kit Extension tools."

description: "Developed weathers' visual effects in NVIDIA Omniverse using Kit Extension tools."
---

<style>
    .slideshow {
    position: relative;
    width: 100%;
    max-width: 600px; /* 調整輪播的最大寬度 */
    height: 310px; /* 調整輪播的高度 */
    margin: 0 auto;
    overflow: hidden;
}

.slide {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    animation: fade 3s infinite; /* 總共 12 秒，無限循環 */
}

.slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* 設定各張照片的動畫時間差 (總秒數須對應上方) */
.slide:nth-child(1) { animation-delay: 0s; }
.slide:nth-child(2) { animation-delay: 1s; }
.slide:nth-child(3) { animation-delay: 2s; }

/* 定義淡入淡出的 CSS 動畫 */
@keyframes fade {
    0% { opacity: 0; }
    35% { opacity: 1; }
    100% { opacity: 0; }
}
</style>
## Rain
First, the number of raindrop particles is set, then a rainfall system is generated. Wind can change the direction in which the raindrops fall. In addition, the particle material is set to water by setting the refractive index (IOR) to 1.33, and cast shadow effects are enabled to enhance realism.
* ### Heavy Rain (particles 5000)

<p align="center">
    <video src="/self/mp4/projects_cg/DigitalEarth/rain_5000.mp4" controls type="video/mov" width="600"></video>
</p>

* ### Light Rain (particles 1000)
<p align="center">
    <video src="/self/mp4/projects_cg/DigitalEarth/rain_1000.mp4" controls type="video/mov" width="600"></video>
</p>

## Fog
<p align="center">
    <video src="/self/mp4/projects_cg/DigitalEarth/fog.mp4" controls type="video/mov" width="600"></video>
</p>

## Cloud
Reconstruct the VDB file using real satellite cloud imagery.
<p align="center">
    <video src="/self/mp4/projects_cg/DigitalEarth/cloud.mp4" controls type="video/mov" width="600"></video>
</p>

The <a href="https://en.wikipedia.org/wiki/Typhoon_Danas_(2025)"> typhoon Danas</a> at July 2025 near Taiwan.
<div class="slideshow">
    <div class="slide"><img src="/self/img/projects_cg/DigitalEarth/202607061400.png" alt="1400"></div>
    <div class="slide"><img src="/self/img/projects_cg/DigitalEarth/202607061500.png" alt="1500"></div>
    <div class="slide"><img src="/self/img/projects_cg/DigitalEarth/202607061600.png" alt="1600"></div>
</div>