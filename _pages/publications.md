---
layout: page
permalink: /publications/
title: publications
years: [1956, 1950, 1935, 1905]
nav: true
---

<div class="publications">

{% for y in (2017..2020) reversed %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
