---
layout: page
title: Wildfire Management
name: Forest Wildfire Management
collection: keywords
keyword: forest-management
permalink: forest-management
description: Wildfire management is the study of managing, predicting, and mitigating risk of forest wildfires.
publish: false
stage: domain
showtitle: true
articles:
  excerpt_type: html
aside: 
    toc: true
---

Forest Wildfire Management is a growing field of major important in Canada and many parts of the world.

<div class="publications">
  <h2>Our Papers on {{ page.name }}</h2> 
{% bibliography -q @*[keywords~={{page.keyword}} && self=1] %}
</div>

<div class="publications">
  <h2>Other Important Papers on {{ page.name }}</h2> 
{% bibliography -q @*[self=0 && keywords~={{page.keyword}}] %}
</div>
