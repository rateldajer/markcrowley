---
layout: page
permalink: /rdgrp-f23/
title: Fall 2023 Reading Group
titleheader: Fall 2023 Reading Group
description: Reading group on the latest topics in Artificial Intelligence
rdgrp-keyword: rdgrp-f23
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
showdiscusseddate: false
---


<hr/>

<h2>Motivation</h2>
Continuation of last year's <a href="/rdgrp-s23/">Transformers Reading Group</a> keeping the theme on Generative AI and RL to start, but who knows where it will go!

<h3>General Reading Groups Tips</h3>
In a **[reading group](/reading-groups/)** everyone takes turns *leading* discussion of a paper each week. Leading discussion can be as simple as having your own annotated notes on Hypothes.is to share and start discussion as we go through it together. Or it could be more involved, including *making slides* to present your overview of the paper's contributions, highlights and weak points.


See the links and notes on paper we have **done** in previous meetings, obtain the link for the **next** paper or look at planned **upcoming** or **potential** future papers, feel free to suggest others or changes in the upcoming order.

<hr/>

{% assign stages = "rd-next, rd-done, rd-upcoming, rd-potential" | split: ", " %}

<b>Jump to stage:</b> {% for rdt in stages %} {% assign t = rdt | split: "-" | slice: 1 %} <a href="#{{rdt}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %} {% endfor %}


<div class="publications by year">
{% for rdt in stages %}
  {% assign t = rdt | split: "-" | slice: 1 %}
  <h2 class="year"><a name="{{rdt}}">{{t}}</a></h2>
    <br/><br/> 
  {% for i in (page.order-start .. page.order-end) reversed %}
      {% bibliography -f research-references-copy -q @*[keywords~=rdgrp-f23, keywords~={{rdt}}, order~={{i}}]* %}
  {% endfor %}
{% endfor %}


</div>

