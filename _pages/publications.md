---
layout: page
permalink: /reading/
title: reading
description: Relevant Texts and Papers for the Course
topics: [text, seminal]
nav: true
---

<div class="publications">

{% for t in page.topics %}
  <h2 >{{t}}</h2>
  {% bibliography -f papers -q @*[keywords={{t}}]* %}
{% endfor %}

</div>
