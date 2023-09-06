---
layout: page
permalink: /reading-groups/
title: Reading Groups
titleheader: Reading Groups
description: List of reading group status
topics: 
- rdgrp-upcoming
- rdgrp-potential
- rdgrp-done
- rdgrp-next
nav: false
showtitle: true
shownotes: true
---

<b>Jump to tag:</b> {% for t in page.topics %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}

<hr/>
todo:
<ul>
<li>sections for each topic of reading group</li>
<li>order by date, or order field</li>
</ul>

<hr/>

<div class="publications">
{% for t in page.topics %}
  <h2><a name="{{t}}">{{t}}</a></h2>
  {% bibliography -f research-references -q @*[keywords~={{t}}]* %}
{% endfor %}


</div>
