---
layout: page
title: topics
titleheader: Research Topics and Domains
permalink: /topics/
nav: true
description: Metapages collecting information on general research topics of interest in the lab. 
showtitle: true
---

Our research can be grouped by intersections of pure research directions, that lead to application ideas, as well as applied domains which lead to new fundamental directions for research. 
Dive into any of the topics below to find out more.

Another way to explore this is to look at all the lab's [Publications Grouped by Research Topics](/pub-by-topic/) or at individual [Research Projects](/projects/).


<div class="projects grid">
  {% assign sorted_topics = site.topics | sort: "importance" %}
  {% for topic in sorted_topics %}
      {% if topic.published %}
          <div class="grid-item">
              {% if topic.redirect %}
                  <a href="{{ topic.redirect }}" target="_blank">
              {% else %}
                  <a href="{{ topic.url | relative_url }}">
              {% endif %}
              <div class="card hoverable">
                {% if topic.img %}
                <img src="{{ topic.img | relative_url }}" alt="topic thumbnail">
                {% endif %}
                <div class="card-body">
                  <h2 class="card-title">{{ topic.title }}</h2>
                  <p class="card-text">{{ topic.description }}</p>
                </div>
              </div>
            </a>
          </div>
      {% endif %}
{% endfor %}
</div>
