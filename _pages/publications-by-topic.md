---
layout: page
permalink: /pub-by-topic/
title: Publication List by Topic
titleheader: Publication List by Topic
description: List of all Publications Grouped by Selected Reseach Topic
topics: 
- anomaly-detection
- bayesian-networks
- causality
- computational-sustainability
- deep-learning
- digital-chemistry
- dimensionality-reduction
- education-research
- ensemble-methods
- fuzzy-logic
- game-theory
- human-robot-interaction
- image-processing
- marl
- mean-field-theory
- multi-agent-systems
- pac-learning
- probabilistic-interence
- reinforcement-learning
nav: false
showtitle: true
---

<b>Jump to Topic:</b> {% for t in page.topics %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}

<div class="publications">
{% for t in page.topics %}
  <h2><a name="{{t}}">{{t}}</a></h2>
  {% bibliography -f papers -q @*[keywords~={{t}}]* %}
{% endfor %}


</div>