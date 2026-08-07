---
layout: page
permalink: /pub-by-topic/
title: Publication List by Topic
titleheader: Publication List by Topic
description: List of all Publications Grouped by Selected Reseach Topic
topics:
  - ai-for-chemistry
  - anomaly-detection
  - autonomous-driving
  - causality
  - computational-sustainability
  - dimensionality-reduction
  - education-research
  - forest-management
  - game-theory
  - human-robot-interaction
  - image-processing
  - machine-ethics
  - multi-agent-reinforcement-learning
  - medical-imaging
  - multi-agent-systems
  - natural-language-processing
  - optimization
  - pac-learning
  - probabilistic-graphical-models
  - reinforcement-learning
  - remote-sensing
  - vehicle-communication
  - vision-language-navigation
  - tree-based-ensembles
hightopics:
  - forest-management
  - machine-ethics
  - human-robot-interaction
  - remote-sensing
  - reinforcement-learning
  - vision-language-navigation
nav: false
showtitle: true
---


<b>Jump to Topic:</b> 
{% for t in page.topics %} <a href="#{{t}}">{% if page.hightopics contains t %} <b>{{t}}</b> {% else %} {{t}} {% endif %}</a> {% if forloop.last==false %} ~ {% endif %} {% endfor %}

*Note that papers will show up in multiple topics.*

<hr/>

Also see:
- [All Published Works](/publications)
- **[Selected Showcase Publications](/showcase)**
- Publications Grouped by Research Topics
- [Defended Theses from the Lab](/theses)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)
- [recent preprints](/preprints)
    - [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)

<hr/>

<div class="publications">
{% for t in page.topics %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
  <br/><br/>
  
  {% bibliography -f papers -q @*[status^=1, self=1, keywords~={{t}}]* %}
{% endfor %}


</div>
