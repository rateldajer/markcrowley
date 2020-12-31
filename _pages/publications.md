---
layout: page
permalink: /reading/
title: reading
description: Relevant Texts and Papers for the Course
topics: [text, seminal]
nav: true
---

The primary textbooks that could be useful are listed here, as well as other seminal papers for different topics we will discuss in the course. For a (nearly) complete list of the reference used in slides throughout the course see the [Course Zotero Reference Group](https://www.zotero.org/groups/2621805/dkma/) page (you may need to request access to join the group to see papers).


<div class="publications">

{% for t in page.topics %}
  <h2 >{{t}}</h2>
  {% bibliography -f papers -q @*[keywords={{t}}]* %}
{% endfor %}

</div>
