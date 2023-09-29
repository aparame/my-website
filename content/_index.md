---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing
design:
  background:
    # Choose a color such as from https://html-color-codes.info
    color: 'navy'
    # Text color (true=light, false=dark, or remove for the dynamic theme color). 
    text_color_light: 
    
sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: features
    content:
      title: Skills
      items:
        - name: C++
          description:
          icon: cpp
          icon_pack: 
        - name: Python
          description:
          icon: python
          icon_pack: fab
        - name: Deep Learning
          description:
          icon: sitemap
          icon_pack: fas
        - name: Controls
          description:
          icon: user-gear
          icon_pack: fas
  - block: experience
    id: Experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Graduate Research Assistant
          company: US Army - VIPR Centre
          company_url: 'https://news.clemson.edu/clemson-u-s-army-gvsc-expand-research-partnership-for-next-generation-autonomous-vehicles/'
          company_logo: 
          location: Clemson, South Carolina
          date_start: '2022-01-11'
          date_end: ''
          description: |2-
              Responsibilities include:
              * Operating with ROS and C++ to develop autonomous navigation algorithms for off-road ground robots.
              * Developed 3D semantically segmented maps with LiDAR and camera sensor data using Python and PyTorch.
              * Led the Perception team of 4 while collaborating with multiple research teams to accomplish project objectives.
                
    
    design:
      columns: '2'
  
  
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Deep Learning
          tag: Deep Learning
        - name: Controls
          tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: markdown
    content:
      title: Gallery
      subtitle: ''
      text: |-
        {{< gallery album="demo" >}}
    design:
      columns: '1'
 
  - block: collection
    content:
      title: Publications
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
    
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
 
  - block: accomplishments
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Certifi&shy;cations'
      subtitle:
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: https://www.udemy.com/certificate/UC-af799482-98ab-4afb-a0ff-09f07821cfcb/
          date_end: ''
          date_start: '2023-05-14'
          description: ''
          organization: Udemy
          organization_url: https://www.udemy.com
          title: Reinforcement Learning Beginner to Master - AI in Python
          url: ''
        - certificate_url: https://www.udemy.com/certificate/UC-da23c056-f8ac-42d7-a443-7358b4351a37/
          date_end: ''
          date_start: '2021-04-13'
          description: Applied Deep Learning and Behavioral Cloning
          organization: Udemy
          organization_url: https://www.udemy.com
          title: The Complete Self-Driving Car Course
          URL: ''
        - certificate_url: https://coursera.org/share/48c80bb9fd0ca11db7c3b3d7da090c1c
          date_end: 
          date_start: '2020-07-02'
          description: ''
          organization: Coursera
          organization_url: https://www.coursera.org
          title: Control of Mobile Robots
          url: ''
    design:
      columns: '2'  
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Please feel free to leave me a message as needed. Thank you for visiting my website.
      # Contact (add or remove contact options as necessary)
      email: adiparamesh@gmail.com

      address:
        street: 
        city: Clemson
        region: SC
        postcode: '29630'
        country: United States
        country_code: US
      
      contact_links:
        - icon: linkedin
          icon_pack: fab
          name: DM Me
          link: 'https://www.linkedin.com/in/aditya-parameshwaran-a3500728a/'
        
      # Automatically link email and phone or display as text?
      autolink: true
      
---
