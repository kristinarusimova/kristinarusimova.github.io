---
layout: page
title: Teaching
permalink: /teaching/
description: 

nav: true
order: 5
---

<div class="projects">

  {% assign sorted_teaching = site.teaching | sort: "importance" %}
  {% for project in sorted_teaching %}
  <h2 class="year">{{project.years}}</h2>
  {% if project.redirect %}
  <a href="{{ project.redirect }}" target="_blank">
  {% else %}
  <a href="{{ project.url | relative_url }}">
  {% endif %}
  <div class="row">
    {% if project.img %}
    <div class="col-sm-3 abbr">
      <img class="rounded float-left z-depth-1" src="{{ project.img | relative_url }}" alt="project thumbnail">
    </div>
    {% endif %}

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
