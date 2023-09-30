---
title: Oral Presentation at SAE World Congress Experience

event: SAE WCX 2023
event_url: https://wcx.sae.org/

location: Detroit, Michigan
  

summary: Presenting my work on guaranteeing Safety in Autonomous Vehicle navigation
abstract: 'The software architecture behind modern autonomous vehicles (AV) is becoming more complex steadily. Safety verification is now an imminent task prior to the large-scale deployment of such convoluted models. For safety-critical tasks in navigation, it becomes imperative to perform a verification procedure on the trajectories proposed by the planning algorithm prior to deployment. Signal Temporal Logic (STL) constraints can dictate the safety requirements for an AV. A combination of STL constraints is called a specification. A key difference between STL and other logic constraints is that STL allows us to work on continuous signals. We verify the satisfaction of the STL specifications by calculating the robustness value for each signal within the specification. Higher robustness values indicate a safer system. Model Predictive Control (MPC) is one of the most widely used methods to control the navigation of an AV, with an underlying set of state and input constraints. Our research aims to formulate and test an MPC controller, with STL specifications as constraints, that can safely navigate an AV. The primary goal of the cost function is to minimize the control inputs. STL constraints will act as an additional layer of constraints that would change based on the scenario and task on hand. We propose using sTaliro, a MATLAB-based robustness calculator for STL specifications, formulated in a receding horizon control fashion for an AV navigation task. It inputs a simplified AV state space model and a set of STL specifications, for which it constructs a closed-loop controller. We test out our controller for different test cases/scenarios and verify the safe navigation of our AV model.'


# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2023-04-19T10:00:00Z'
# date_end: '2030-06-01T15:00:00Z'
# all_day: false

# Schedule page publish date (NOT talk date).
# publishDate: '2017-01-01T00:00:00Z'

authors: []
tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'SAE WCX Congress, Detroit'
  focal_point: Right

links:
url_code: ''
url_pdf: ''
url_slides: 'https://docs.google.com/presentation/d/1iYR8xlaLWW_LBy45rsd_VEJTerPy_VyL/edit?usp=sharing&ouid=115261715409316286458&rtpof=true&sd=true'
url_video: ''

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
  - example
---

The [slides](https://docs.google.com/presentation/d/1iYR8xlaLWW_LBy45rsd_VEJTerPy_VyL/edit?usp=sharing&ouid=115261715409316286458&rtpof=true&sd=true) for the presentation can be viewed online here. They are best viewed in presentation mode.

