---
layout: page
title: topics
titleheader: Topics
permalink: /topics/
nav: true
description: Metapages collecting information on topics of interest in the lab. 
showtitle: true
---

<div class="projects grid">
  {% assign sorted_topics = site.topics | sort: "title" %}
  {% for topic in sorted_topics %}
      {% if topic.publish %}
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