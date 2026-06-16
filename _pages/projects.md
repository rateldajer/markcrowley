---
layout: page
title: projects
titleheader: Application Domains and Active Projects
permalink: /projects/
description: Ongoing projects and domains of application within the lab.
nav: true
showtitle: true
---

Also see broader areas of research based on [Research Topics and Domains](/topics/)

<div class="projects grid">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
  {% if project.published %}

  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
         {% if project.cardtitle %}
              <h2 class="card-title">{{ project.cardtitle }}</h2>
          {% else %}
              <h2 class="card-title">{{ project.title }}</h2>
          {% endif %}
          <p class="card-text">{{ project.description }}</p>

        </div>
      </div>
    </a>
  </div>
{% endif %}
{% endfor %}

</div>