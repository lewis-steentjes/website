---
title: "Multiphase LED Driver"
date: 2020-11-07T10:18:56+13:00
description: "I programmed an LED driver using an Arduino Nano."
draft: false
author: Lewis
authorEmoji: 🦉
tags: 
- Project
image: images/icons/3_phase_AC_waveform.png
---

For this project, I wanted to create an LED driver that could control multiple LEDs such that they would light up in order from one to the next and simulate motion of the light. I want to use something like this at some point for use in decorations.

To accomplish this, I wrote a program that would use a generic wave function and a time input to control the LEDs by a given phase differential. This turned out great, as it's very easy to test out different ways of lighting up the LEDs. 

Since the phase differential can be controlled it's also a very versatile system for use in decorations. For instance, if I design a decoration that moves the LED emissions in a circular pattern and uniformly spread both the LEDs then a uniform phase distribution is preferred. However, if the LEDs are spread non-uniformly  around the circle then a phase distribution that better describes where the individual LEDs are on the circle may look better.

---

Full source code is available [here](https://github.com/lpsteentjes/GeneralWavePWM-Arduino/blob/main/generalPurposeOscillatingPWM.ino).

I made a small video of some of the potential different waveforms in action and how they look at a given frequency.

{{< youtube GL1WlP2LXDg >}}