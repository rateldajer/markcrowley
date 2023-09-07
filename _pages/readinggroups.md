---
layout: page
permalink: /reading-groups/
title: Reading Groups
titleheader: Reading Groups
description: List of reading group status
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
---

{% assign stages = "next, done, upcoming, potential" | split: ", " %}
<b>Jump to tag:</b> {% for t in page.topics %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}

<hr/>


<div class="publications by year">
{% for t in stages %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
  {% for i in (page.order-start .. page.order-end) reversed %}
      {% bibliography -f research-references -q @*[keywords~={{t}}, order~={{i}}]* %}
  {% endfor %}
{% endfor %}


</div>

<!-- TODO
- fill in date-discussed in rest of bibtex, and order
- add nots from overleaf to bibtex annote field
-->

