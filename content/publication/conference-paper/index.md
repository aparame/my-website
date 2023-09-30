---
title: 'Safety Verification and Navigation for Autonomous Vehicles Based on Signal Temporal Logic Constraints'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Yue Wang


# Author notes (optional)
author_notes:
  - 'Equal contribution'


date: '2023-01-13T00:00:00Z'
doi: 'https://doi.org/10.4271/2023-01-0113'

# Schedule page publish date (NOT publication's date).
publishDate: ''

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: In *SAE Technical Papers*
publication_short: 

abstract: 'The software architecture behind modern autonomous vehicles (AV) is becoming more complex steadily. Safety verification is now an imminent task prior to the large-scale deployment of such convoluted models. For safety-critical tasks in navigation, it becomes imperative to perform a verification procedure on the trajectories proposed by the planning algorithm prior to deployment. Signal Temporal Logic (STL) constraints can dictate the safety requirements for an AV. A combination of STL constraints is called a specification. A key difference between STL and other logic constraints is that STL allows us to work on continuous signals. We verify the satisfaction of the STL specifications by calculating the robustness value for each signal within the specification. Higher robustness values indicate a safer system. Model Predictive Control (MPC) is one of the most widely used methods to control the navigation of an AV, with an underlying set of state and input constraints. Our research aims to formulate and test an MPC controller, with STL specifications as constraints, that can safely navigate an AV. The primary goal of the cost function is to minimize the control inputs. STL constraints will act as an additional layer of constraints that would change based on the scenario and task on hand. We propose using sTaliro, a MATLAB-based robustness calculator for STL specifications, formulated in a receding horizon control fashion for an AV navigation task. It inputs a simplified AV state space model and a set of STL specifications, for which it constructs a closed-loop controller. We test out our controller for different test cases/scenarios and verify the safe navigation of our AV model.
11 citation on Dimensions.'


tags:
- Source Themes
  

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_code: 'https://github.com/aparame/SAE_STL/tree/main'
url_slides: 'https://docs.google.com/presentation/d/1iYR8xlaLWW_LBy45rsd_VEJTerPy_VyL/edit?usp=sharing&ouid=116668006117678886591&rtpof=true&sd=true'


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

