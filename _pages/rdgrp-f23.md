---
layout: page
permalink: /rdgrp-f23/
title: Fall 2023 Reading Group
titleheader: Fall 2023 Reading Group
description: Reading group on Causality, RL and Transformers in the lab in Fall 2023
rdgrp-bib-file: rdgrp-f23
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
---


<hr/>

<h2>First meeting: Oct 23, 2023!</h2>
**Location:** In person in EIT-3101 or you can join online via Teams. 

All are welcome.


<h2>Motivation</h2>
Over the summer we had a great discussion with the <a href="/rdgrp-s23/">Transformers Reading Group</a> going through some of the foundational papers on the popular new deep learning paradigm.
But we know we only scratched the surface! 

This term, we'll dive into a few side topics related to this new area but focussing on topics people are working on in the lab such as 
<a href="/causality">Causality</a> and 
<a href="/reinforcement-learning">Reinforcement Learning</a>. 

<h3>Resources</h3>
This github page has a quite extensive list of papers and references on the topic so seems as good a place as any to start:
<ul><li>
<a href="https://github.com/Hannibal046/Awesome-LLM#milestone-papers">Awesome LLM Milestone Papers</a>
</li></ul>

<h3>General Reading Groups Tips</h3>
In a **[reading group](/reading-groups/)** everyone takes turns *leading* discussion of a paper each week. Leading discussion can be as simple as having your own annotated notes on Hypothes.is to share and start discussion as we go through it together. Or it could be more involved, including *making slides* to present your overview of the paper's contributions, highlights and weak points.


See the links and notes on paper we have **done** in previous meetings, obtain the link for the **next** paper or look at planned **upcoming** or **potential** future papers, feel free to suggest others or changes in the upcoming order.

<hr/>

{% assign stages = "next, done, upcoming, potential" | split: ", " %}

<b>Jump to stage:</b> {% for t in stages %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}


<div class="publications by year">
{% for t in stages %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
  {% for i in (page.order-start .. page.order-end) %}
      {% bibliography -f rdgrp-f23 -q @*[keywords~={{t}}, order~={{i}}]* %}
  {% endfor %}
{% endfor %}


</div>


