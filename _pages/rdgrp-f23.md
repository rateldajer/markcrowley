---
layout: page
permalink: /rdgrp-w24/
title: Winter 2024 Reading Group
titleheader: Winter 2024 Reading Group
description: Reading group on the latest topics in Artificial Intelligence
rdgrp-bib-file: rdgrp-w24
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
---


<hr/>

<h2>First meeting: ???, 2024!</h2>
**Location:** TBD. 

All are welcome.


<h2>Motivation</h2>
Continuation of last year's <a href="/rdgrp-s23/">Transformers Reading Group</a> keeping the theme on Generative AI and RL to start, but who knows where it will go!

<h3>General Reading Groups Tips</h3>
In a **[reading group](/reading-groups/)** everyone takes turns *leading* discussion of a paper each week. Leading discussion can be as simple as having your own annotated notes on Hypothes.is to share and start discussion as we go through it together. Or it could be more involved, including *making slides* to present your overview of the paper's contributions, highlights and weak points.


See the links and notes on paper we have **done** in previous meetings, obtain the link for the **next** paper or look at planned **upcoming** or **potential** future papers, feel free to suggest others or changes in the upcoming order.

<hr/>

{% assign stages = "next, done, upcoming, potential" | split: ", " %}

<b>Jump to stage:</b> {% for t in stages %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}


<div class="publications by year">
{% for t in stages %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
    <br/><br/> 
  {% for i in (page.order-start .. page.order-end) %}
      {% bibliography -f rdgrp-w24 -q @*[keywords~="decision-transformer",  keywords~={{t}}, order~={{i}}]* %}
  {% endfor %}
{% endfor %}


</div>


