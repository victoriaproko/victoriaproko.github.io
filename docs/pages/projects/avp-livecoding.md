---
layout: project-page
title: "Embodied-Algorave"
short_description: "Designing & prototyping an XR creative tool for Embodied Musical Development for Apple Vision Pro."
role: "UX Researcher · Interaction Designer · Developer"
tools: "Reality Composer Pro, Swift, xrOS, Figma"
timeline: "Fall 2024 — Spring 2025"
image: 
permalink: /projects/avp-livecoding/
---

## Overview
This project explores the key question: **how can embodied XR live-coding environments function as design probes for deepening one’s connection to music?**

Live coding is the practice of writing and modifying musical code in real time. It has gained popularity in recent years through events such as algoraves, where performers generate sound by typing symbolic patterns while audiences listen and watch the evolving code on a projected screen. Although compelling, this format only allows for cognitive and auditory engagement with liveness, lacking physical involvement.

---

## Inquiry

Our team wondered whether XR, with its immersive spatial audio, precise hand tracking, and expressive 3D visuals, could bridge this gap and reimagine how music is felt. What happens when rhythm is visually present in the air around the performer? When gestures can directly shape a musical pattern? When movement itself becomes part of the composition process?

Our goal is to **investigate how immersive environments affect users’ experience of music. By allowing performers to see, touch, and move through musical structures, embodied XR transforms live coding from a symbolic interaction into a physically grounded practice. In this project, we employ the HCI framework of design probes to investigate how spatial computing technologies may support and enhance creative flow during live music composition.**

We have developed a prototype demonstrating live integration between Strudel (for algorithmic music), Swift logic, and RealityKit-based spatial visuals. Continued access to the Apple Vision Pro is essential for advancing this research.

---

## Process

### Research
Our project is informed by several key areas of research in HCI.

<u>Design Probe</u>

  We reference the HCI frameworks on design probes, which are objects intentionally designed to invite participant reflection, as both tools for design and tools for exploration. Particularly, we consider our design from four key properties:
  
  * **Thematic openness vs boundedness:** giving enough freedom to explore, but enough constraint to direct attention and make the task completable
  * **Materiality:** the physical qualities of the probe (form, materials, affordances) that scaffold reflection
  * **Pace:** how quickly or slowly participants engage with it
  * **Challenge:** the degree of difficulty or provocation in the probe

<u>Cognitive load theory</u>

  We distinguish between **intrinsic load** (the inherent complexity of musical structures and pattern relationships) and **extraneous load** (unnecessary mental effort introduced by interface or representation). The framework of effective cognitive load provides a lens for evaluating how XR may redistribute cognitive effort, informing design on complexity.
  
<u>Live coding movement</u>

  We align our project with the key principles of liveness and transparency of code, referencing key figures like Alex Mclean, Nick Collins, Julian Rohrhuber, Roxanne Harris, etc…

<u>Embodied interaction</u>

  We recognize the ways XR introduces spatial, gestural, and multisensory feedback channels that shape how users experience their body in immersive spaces.
  

### Ideation & Storyboarding
How ideas formed, sketches, decisions:

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 20px;">
  
  <div style="border: 1px solid #eee; border-radius: 8px; overflow: hidden;">
    <img src="/assets/sketch1 2.png" alt="Sketch 1" style="width: 100%; display: block;">
  </div>

  <div style="border: 1px solid #eee; border-radius: 8px; overflow: hidden;">
    <img src="/assets/sketch2 2.png" alt="Sketch 2" style="width: 100%; display: block;">
  </div>

  <div style="border: 1px solid #eee; border-radius: 8px; overflow: hidden;">
    <img src="/assets/sketch3 2.png" alt="Sketch 3" style="width: 100%; display: block;">
  </div>

  <div style="border: 1px solid #eee; border-radius: 8px; overflow: hidden;">
    <img src="/assets/sketch4 2.png" alt="Sketch 4" style="width: 100%; display: block;">
  </div>

</div>

### Technical Scaffolding

Over the course of this semester, we focused on scoping the conceptual and technical possibilities. We began by experimenting with established live-coding tools like **TidalCycles and SuperCollider,** or the possibility of building our own sound pattern library. It became clear that most of these systems relied on too many layers of external processes (Haskell interpreters, SuperDirt/SuperCollider audio servers, and complex OSC routing), which didn’t integrate cleanly with **RealityKit and Swift.** We chose **Strudel** for music generation due to its lightweight, fully self-contained JavaScript architecture, its clean API surface, and its use of WebAudio for low-latency timing and synthesis.

Now, we established a working pipeline in which RealityKit manages spatial visuals and gesture input. Swift processes these interactions and communicates through a JavaScript bridge to a WebView running Strudel. Strudel then generates music via WebAudio.

### Our next steps

The next step of the project is to create an application for user studies. This involves aligning our design concepts with the technical system and implementing different mappings between gesture, spatial arrangement, and musical structure. Over the next year, we hope to gather qualitative and quantitative insights into how immersive live coding shapes creative flow and musical understanding.


---
