---
title: Example Project
summary: An example of using the in-built project page.
tags:
  - Deep Learning
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Autonomous RC Car
  focal_point: Smart

links:
url_code: 'https://github.com/aparame/AI_RC_Car'
url_pdf: 'https://drive.google.com/file/d/1PvhqNhtHjqh15I8arVBqJ329xoe5nkOL/view?usp=sharing'
url_slides: 'https://docs.google.com/presentation/d/1CcWqkM2MQmbkFz47-91WTZGl0ZzYxxNljZTX2ZMmXg8/edit?usp=sharing'
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

*Abstract*: The aim of this group project is to implement the autonomous driving skills learned in class to develop an autonomous lane-keeping and road sign-detecting RC car in a known environment. The tasks of the project were broken down into sections based on the requirements for successfully navigating the RC bot around the track. We began by identifying the layout of the track and determining the best camera locations for the bot. The image data was pre-processed to be used by the lane-keeping and sign-detection algorithms. A CNN based on the ResNet architecture was trained for sign detection using images captured by the bot’s secondary camera. The result was an autonomous RC bot that was successfully able to identify and navigate through the track while detecting the STOP and SCHOOL signs accurately and reacting appropriately.
