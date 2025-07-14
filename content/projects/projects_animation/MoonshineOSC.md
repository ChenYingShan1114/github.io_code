---
author: "Ying-Shan Chen"
title: "Light Controlled by Sound in Real-time"
date: '2025-03-14'
categories: [
    "animation",
    "intern project"
]
tags: [
    "Unreal Engine",
    "ToughDesigner",
    "Open Sound Control",
    "Audio Visualization"
]
resume: "Created a two-part interactive project combining Unreal Engine and TouchDesigner. Designed a detailed virtual room with lighting and camera sequencing, then integrated audio analysis to drive a blueprint-based sparkling wall lamp."
description: "A two-part project combining Unreal Engine and TouchDesigner: I first designed a detailed virtual room with lighting and camera sequencing, then connected audio analysis from TouchDesigner to control a blueprint-driven sparkling wall lamp."
---
<h3> 🔧 Step 1: Room Construction and Cinematic Setup </h3>
Using assets from Fab, I built a 3m × 3m × 5m interior space in Unreal Engine. The scene includes a variety of lighting elements:

• Environmental light simulates the overall ambient condition and expresses the transition between daytime and nighttime.

• Indirect (indirectional) lighting is added to fill in darker areas, ensuring that key parts of the room remain visible without relying on harsh direct light.

• Bolt-generated light sources are placed as decorative and functional fixtures within the room.

• A sparkling wall lamp that would later be controlled by sound

To present the room in a cinematic way, I also created a level sequence that animates both camera movement and lighting transitions, allowing viewers to fully appreciate the room’s structure and visual details.

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/anpu47o5NCM?si=08EzlKesLL2lVvWi&autoplay=1&loop=1&playlist=anpu47o5NCM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

<h3> 🎵 Step 2: Audio-Driven Lighting with TouchDesigner (via Open Sound Control) </h3>
In the second part of the project, I used TouchDesigner to perform real-time audio analysis, extracting data from a music track. The analyzed sound features—such as beat intensity or frequency response—were sent to Unreal Engine using Open Sound Control (OSC), a protocol for real-time communication between software.

Inside Unreal Engine, I created a custom Blueprint for the sparkling wall lamp, which listens to the OSC signals and triggers lighting effects based on the incoming audio data. As a result, the lamp sparkles dynamically in sync with the music, bringing the environment to life through audiovisual interaction.

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/rsNS2LIh1pQ?si=giXSvJEt_T979MlC&autoplay=1&loop=1&playlist=rsNS2LIh1pQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

This project highlights how I integrate creative scene composition, technical lighting design, and real-time audio interactivity—skills essential for technical art and virtual production.