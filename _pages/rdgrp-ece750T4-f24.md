---
layout: page
permalink: /rdgrp-ece750T4-f24/
title: ECE750T4 Reinforcement Learning - Reading List
titleheader: ECE750T4 Reinforcement Learning - Reading List
description: Reading list for the Grad Topics course on Reinforcement Learning (ECE 750 Topic 4) for Fall 2024
rdgrp-keywords: rdgrp-ece750T4-f24
order-start: 1
order-end: 50
nav: false
showtitle: true
shownotes: true
showbiborder: true
showdiscusseddate: true
---

<h2>Introduction</h2>
This course will have two components, which shift focus over the term. The first component will be lectures and work problems about the fundamentals of Reinforcement Learning (RL).

The second component will be communal presentation and discussion of research papers on advanced topics in RL. 
The papers will be read by all, presented briefly by a student, and then discussed by everyone, led by the presenting student, for half of the class period.

This second component is structured around the common grad school practice of Reading Groups, see more information below or see the pages for some <a href="/reading-groups">previous reading groups here</a>.

<h3>Reading Groups Tips</h3>

In a **[reading group](/reading-groups/)** everyone takes turns *leading* discussion of a paper each week. Leading discussion can be as simple as having your own annotated notes on Hypothes.is to share and start discussion as we go through it together. Or it could be more involved, including *making slides* to present your overview of the paper's contributions, highlights and weak points.


<hr/>

<h2>The Reading List</h2>

Papers listed below are ones that we are planning to read throughout the term. The order is given but this shouldn't be considered too strict, some papers could be done in different orders. In general, we should read papers which are foundational for others first.

### What you need to do
If you are a student in this course you need to do the following:
- Create a Hypothes.is account
- Pick the papers you will be reading, presenting, and leading discussion of
    - PhD Students: choose two papers, one of them near the start to set a good example!
    - Master's Students: choose at least one paper
- Then read the paper in detail, use Hypothes.is to make annotations for yourself and to guide others. Use the Hypothes.is course group you were all invited to do to this.
- Prepare to present the main points of the paper, and guide discussion through the parts that are surprising, challening, interetsing, or that you don't understand.
- The class discussion of the paper should help everyone, including you and the prof come away with a better understanding and evaluation of this publication


---

### Each Week
See the links and notes on paper we have **done** in previous classes, obtain the link for the **next** paper or look at planned **upcoming** or **potential** future papers, feel free to suggest others or changes in the upcoming order. Note: `reference` indicates publications that no one needs to volunteer to present, they mostly books and other resources that may also prove useful in understanding the course topic. `optional` publications won't be discussed if no one volunteers to present them.

{% assign stages = "next week, earlier, middle, later, optional, complete, reference" | split: ", " %}

<b>Jump to stage:</b> {% for t in stages %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}


<div class="publications by year">
{% for t in stages %}
  <h2 class="year"><a name="{{t}}">{{t}}</a></h2>
    <br/><br/> 
  {% for i in (page.order-start .. page.order-end) %}
      {% bibliography -f research-references-copy -q @*[keywords~=rdgrp-ece750T4-f24, keywords~={{t}}, order~={{i}}]* %}
  {% endfor %}
{% endfor %}


</div>

