---
title: Autonomous Rail-Bot for Data Collection
summary: Build an autonomous bot from the ground up, that runs on railway tracks to collect telemetric and perception data. 
tags:
  - Robotics
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Autonomous Rail-Bot
  focal_point: Smart

links:
url_code: 'https://github.com/aparame/Autonomous_RailBot'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

*Abstract*: At Purdue University, I am currently engaged in the development of an autonomous railway bot designed to traverse railway tracks autonomously while simultaneously collecting crucial sensor data through the implementation of LiDAR, stereo cameras, and an Inertial Measurement Unit (IMU) for tasks such as track detection and obstacle avoidance. The primary objective of this bot is to proficiently map the railway tracks and generate a high-definition 3D map of its surrounding environment. Notably, the design of the bot is optimized to allow a single operator to carry it on their back, enhancing its mobility. Furthermore, the bot is equipped to accommodate an additional payload of 30 pounds, intended for sensors aimed at detecting faults and cracks on the track surface. The computational aspects are handled by an Nvidia Jetson AGX, serving as the computing platform to receive, process, and relay sensor data through Robot Operating System (ROS) commands to the motor controllers. The acquired perception data will be utilized to construct a dataset for training a Convolutional Neural Network (CNN), specifically tailored for the recognition of traffic signs along the railway track. The intricate blend of computer science and mechatronics involved in this project has significantly advanced my proficiency in electronics and programming
