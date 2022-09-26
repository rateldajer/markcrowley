---
layout: page
title: (draft) All the Keywords 
titleheader: All the keywords
permalink: /keywords/
nav: true
description: Trying to sort out all the different types of keywords. 
showtitle: true
---

todo: isn't there a page already somewhere with all the keywords/topics/methods/domains on all pages?


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
