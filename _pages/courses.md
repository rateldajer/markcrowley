---
layout: page
title: courses-list
description: Courses being taught by Mark Crowley.
nav: false
showtitle: true
---

<div class="projects grid">
  {% assign sorted_courses = site.courses | sort: "importance" %}
  {% for course in sorted_courses %}
  <div class="grid-item">
    {% if course.redirect %}
    <a href="{{ course.redirect }}" target="_blank">
    {% else %}
    <a href="{{ course.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if course.img %}
        <img src="{{ course.img | relative_url }}" alt="course thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ course.title }}</h2>
          <p class="card-text">{{ course.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if course.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ course.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if course.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ course.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
