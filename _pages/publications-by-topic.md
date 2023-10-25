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
- bayesian-networks
- causality
- computational-sustainability
- data-reduction
- deep-learning
- digital-chemistry
- digital-pathology
- dimensionality-reduction
- education-research
- ensemble-methods
- forest-management
- fuzzy-logic
- game-theory
- human-robot-interaction
- image-processing
- invasive-species-management
- search-and-rescue
- manifold-learning
- marl
- mean-field-theory
- medical-imaging
- multi-agent-systems
- nlp
- optimization
- pac-learning
- probabilistic-inference
- reinforcement-learning
- vehicle-communication
nav: false
showtitle: true
---


<b>Jump to Topic:</b> {% for t in page.topics %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}

*Note that papers will show up in multiple topics.*

<hr/>

Also see:
- [All Published Works](/publications)
- **[Selected Showcase Publications](/showcase)**
- [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)

<hr/>

<div class="publications">
{% for t in page.topics %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
  <br/><br/>
  
  {% bibliography -f papers -q @*[status^=1, keywords~={{t}}]* %}
{% endfor %}


</div>
