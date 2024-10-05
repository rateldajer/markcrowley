---
layout: page
permalink: /rdgrp-ece750T4-f24/
title: ECE750T4 Reinforcement Learning - Reading List
titleheader: ECE750T4 Reinforcement Learning - Reading List
description: Reading list for the Grad Topics on Reinforcement Learning (ECE 750 Topic 4) for Fall 2024
rdgrp-keywords: rdgrp-ece750T4-f24
order-start: 1
order-end: 10
nav: false
showtitle: true
shownotes: true
showbiborder: true
showdiscussed: true
---

<h2>Introduction</h2>
This course will have two components, which shift focus over the term. The first component will be lectures and work problems about the fundamentals of Reinforcement Learning (RL).

The second component will be communal presentation and discussion of research papers on advanced topics in RL. 
The papers will be read by all, presented briefly by a student, and then discussed by everyone, led by the presenting student, for half of the class period.

This second component is structured around the common grad school practice of Reading Groups, see more information below or see the pages for some <a href="/reading-groups">previous reading groups here</a>.

<h3>Reading Groups Tips</h3>

In a **[reading group](/reading-groups/)** everyone takes turns *leading* discussion of a paper each week. Leading discussion can be as simple as having your own annotated notes on Hypothes.is to share and start discussion as we go through it together. Or it could be more involved, including *making slides* to present your overview of the paper's contributions, highlights and weak points.


<hr/>

<h2>The Course Reading List</h2>

Papers listed below are ones that we are planning to read throughout the term. An order **[n]** is sometime listed but this is just a rough guide. In general, if one paper is base don work in an older paper, the older paper should be discussed first, or the same week.

### What you need to do
If you are a student in this course you need to do the following:
- Create a Hypothes.is account and sign up for the <a href="https://hypothes.is/groups/DM67BYBG/uwece-rl-course-reading">course group on Hypothes.is</a> so you and everyone in the class can see our shared annotations 
- Pick the papers you will be reading, presenting, and leading discussion of and *sign up* **(sign-up process TBD)**
    - PhD Students: choose two papers, one of them near the start to set a good example!
    - Master's Students: choose at least one paper
- Then read the paper in detail, use Hypothes.is to make annotations for yourself and to guide others. Use the Hypothes.is course group you were all invited to do to this.
- Prepare to present the main points of the paper, and guide discussion through the parts that are surprising, challening, interetsing, or that you don't understand.
- The class discussion of the paper should help everyone, including you and the prof come away with a better understanding and evaluation of this publication



### Papers We'll Be Reading

{% assign stages = "rd-current, rd-early, rd-middle, rd-later, rd-done" | split: ", " %}

See the links below for information about and notes on papers 
planned readings for some time in the `early`, `middle`, or `later` part of the course,
obtain the link for the `current` reading for this week, 
or for those that are `done` from previous weeks.

<i>(Jump to a stage and sign up to lead a paper)</i> <br/>
{% for rdt in stages %} {% assign t = rdt | split: "-" | slice: 1 %} <a href="#{{rdt}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %} {% endfor %}



<div class="publications by year">
{% for rdt in stages %}
  {% assign t = rdt | split: "-" | slice: 1 %}
  <h2 class="year"><a name="{{rdt}}">{{t}}</a></h2>
    <br/><br/> 
      {% bibliography -f research-references-copy -q @*[keywords~=rdgrp-ece750T4-f24, keywords~={{rdt}}]*  %}
{% endfor %}


</div>

<hr/>
## Other Reading
The following sections list  publications that no one needs to volunteer to present, they mostly `reference` papers and books, simulation environment descriptions, or other resources that may also prove useful in understanding the course topic. 
`potential` publications probably won't be discussed if no one volunteers to present them.

{% assign otherpapers = "rd-reference, rd-foundational, rd-environment, rd-potential" | split: ", " %}
<i>(Not to sign up for, just for reference and interest)</i><br/>
{% for rdt in otherpapers %} {% assign t = rdt | split: "-" | slice: 1 %} <a href="#{{rdt}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %} {% endfor %}

<div class="publications by year">
{% for rdt in otherpapers %}
  {% assign t = rdt | split: "-" | slice: 1 %}
  <h2 class="year"><a name="{{rdt}}">{{t}}</a></h2>
    <br/><br/> 
      {% bibliography -f research-references-copy -q @*[keywords~=rdgrp-ece750T4-f24, keywords~={{rdt}}]* %}
{% endfor %}


</div>

