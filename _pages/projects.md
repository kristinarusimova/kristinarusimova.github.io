---
layout: page
title: projects
permalink: /projects/
description: 
nav: true
---

<div class="projects">

  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
  <h2 class="year">{{project.years}}</h2>
  {% if project.redirect %}
  <a href="{{ project.redirect }}" target="_blank">
  {% else %}
  <a href="{{ project.url | relative_url }}">
  {% endif %}
  <div class="row">
    <div class="col-sm-3 abbr">
      {% if project.img %}
      <img class="rounded float-left z-depth-1" src="{{ project.img | relative_url }}" alt="project thumbnail">
      {% endif %}
    </div>

    <div class="col-sm-7">
      <span class="title">{{project.title }}</span>
      {% if project.location %}
      <span class="location">{{project.location }}</span>
      {% endif %}
      <span class="description">
          {{ project.description }}
      </span>
    </div>
  </div>
  </a>
{% endfor %}

</div>