---
layout: page
title: Manifold Learning
permalink: /manifold-learning/
name: Manifold Learning
keyword: manifold-learning
description: Manifold learning looks at ways to automatically extract meaningful features, dimensions or subspaces from data in order to build better models, expand data, reduce data, etc.
stage: field
showtitle: true
aside: 
    toc: true
---

<div class="publications">
  <h2>Our Papers on {{ page.name }}</h2> 
{% bibliography -q @*[keywords~={{page.keyword}} && self=1] %}
</div>

<div class="publications">
  <h2>Other Important Papers on {{ page.name }}</h2> 
{% bibliography -q @*[self=0 && keywords~={{page.keyword}}] %}
</div>
