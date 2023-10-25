---
layout: page
permalink: /rdgrp-s23/
title: Spring 2023 Reading Group
titleheader: Spring 2023 Reading Group
description: Reading group on Transformers in the lab in Spring 2023
rdgrp-bib-file: rdgrp-s23
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
---

<h2>Reading Groups Tips</h2>
In a **[reading group](/reading-groups/)** everyone takes turns *leading* discussion of a paper each week. Leading discussion can be as simple as having your own annotated notes on Hypothes.is to share and start discussion as we go through it together. Or it could be more involved, including *making slides* to present your overview of the paper's contributions, highlights and weak points.


<hr/>

<h2>Spring 2023 - Transformers Reading Group</h2>

<h3>Motivation</h3>

AI research has been undergoing since the dawn of computer science itself, and Deep Learning has seen an uninterrupted, and accelerating wave of advancing abilities for over 12 years since the public breakthroughs of CNNs in 2012. Yet still, many people, including AI/ML researchers have been surprised at the abilities of the generative models that have been released since summer 2022 by OpenAI, Facebook, Google and others. The recent systems all rely in various ways on the Transformer model {% cite vaswani2017neurips %}. 

<h3>Resources</h3>
This github page has a quite extensive list of papers and references on the topic so seems as good a place as any to start:
<ul><li>
<a href="https://github.com/Hannibal046/Awesome-LLM#milestone-papers">Awesome LLM Milestone Papers</a>
</li></ul>

<hr/>

See the links and notes on paper we have **done** in previous meetings, obtain the link for the **next** paper or look at planned **upcoming** or **potential** future papers, feel free to suggest others or changes in the upcoming order.

{% assign stages = "next, done, upcoming, potential" | split: ", " %}

<b>Jump to stage:</b> {% for t in stages %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}


<div class="publications by year">
{% for t in stages %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
    <br/><br/> 
  {% for i in (page.order-start .. page.order-end) reversed %}
      {% bibliography -f  rdgrp-s23 -q @*[keywords~={{t}}, order~={{i}}]* %}
  {% endfor %}
{% endfor %}


</div>

