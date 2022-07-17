---
title: "Plant Monitoring System"
date: 2022-02-03T20:54:00+13:00
description: "The beginning of a system for remotely monitoring plant growth"
draft: false
hideToc: false
enableToc: false
enableTocContent: false
author: Lewis
authorEmoji: 🦉
tags: 
- Project
image: images/icons/camera_01_04.png
---

So I accidentally found myself buying a Raspberry Pi 400 and now I need something to do with it 😅. The current plan is to use NodeJS to create a web app which will allow provide visual updates via webcam, long-term light-level statistics, automated watering and manual watering via web interface. 

{{< img src="/images/plants/webtest01.png" alt="{Screenshot of web app}" width="500px" height="375px">}}

</br>

This weekend I successfully set up an SSH for my RaspberryPi and hosted a webpage which triggered my webcam to take a photo and update the image on the webpage. Later down the line, this will be used in a permanent setup to view plants. 

Next in line, I will use some form of solar cells to analyse light levels and source a pump and hose for misting the plants from a reservoir.