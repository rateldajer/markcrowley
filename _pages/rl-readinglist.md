---
layout: page
permalink: /rl-reading-list/
title: Reinforcement Learning - Reading List
titleheader: Reinforcement Learning - Reading List
description: Reading list for Reinforcement Learning 
rdgrp-keywords: rdgrp-ece750T4-f24
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
showdiscussed: true
---


The papers listed below are a loose superset of the ones I try to cover, or have students present, throughout the term during my . 

> *And Lo, the legends tell us, that before there was even the DQN, there was the incredible VFAs, and before this the Great Age of the Value Tables themselves.*

`Foundational` papers fill the first part of the list.
Once we enter the era of **Deep Reinforcement Learning**, the papers are grouped into `early`, `middle`, or `later` for how they would fall in a graduate course on Advanced RL such as my [RL Courses (ECE 457C/657C)](/rlgradcourse/). Other topics categories relate to general `reference`, papers mostly about `environments` to test out RL algorithms, or `potential` paper for future reading.
Further ordering with **[n]** is sometime listed but this is just a rough guide. In general, if one paper is based on work in an older paper, the older paper should be discussed first, or the same week.

{% assign stageslinks = "rd-foundational, rd-early, rd-middle, rd-later, rd-reference, " | split: ", " %}

<i>(You can jump to any stage with these links to find a paper)</i> <br/>
{% for rdt in stageslinks %} {% assign t = rdt | split: "-" | slice: 1 %} <a href="#{{rdt}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %} {% endfor %}

{% assign stages = "rd-foundational, rd-early, rd-middle, rd-later" | split: ", " %}


<div class="publications by year">
{% for rdt in stages %}
  {% assign t = rdt | split: "-" | slice: 1 %}
  <h2 class="year"><a name="{{rdt}}">{{t}}</a></h2>
    <br/><br/> 
      {% bibliography -f research-references-copy -q @*[keywords~=rdgrp-ece750T4-f24, keywords~={{rdt}}]*  %}
{% endfor %}
</div>


</div>

<hr/>
## Other Reading
The following sections list additional relevant publications that are optional for my course. They mostly `reference` papers and books, simulation environment descriptions, or other resources that may also prove useful in understanding the course topic. 
`potential` publications are even more optional, and probably wouldn't have time to be discussed in the course unless someone volunteers to present them.

{% assign otherpapers = "rd-reference, rd-environment, rd-potential" | split: ", " %}
{% for rdt in otherpapers %} {% assign t = rdt | split: "-" | slice: 1 %} <a href="#{{rdt}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %} {% endfor %}

<div class="publications by year">
{% for rdt in otherpapers %}
  {% assign t = rdt | split: "-" | slice: 1 %}
  <h2 class="year"><a name="{{rdt}}">{{t}}</a></h2>
    <br/><br/> 
      {% bibliography -f research-references-copy -q @*[keywords~=rdgrp-ece750T4-f24, keywords~={{rdt}}]* %}
{% endfor %}
</div>

