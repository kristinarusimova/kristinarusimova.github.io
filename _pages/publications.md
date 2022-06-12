---
layout: page
permalink: /publications/
title: Publications

nav: true
order: 2
---

<div class="publications">
<!-- Get the current year as an integer -->
{% assign thisyear = site.time | date: '%Y' | to_integer %}
<!-- Loop from 2017 to current year -->
{% for y in (2017..thisyear) reversed %}

  <!-- Get number of citations for this year in the loop -->
  <!-- Gross workaround for https://github.com/inukshuk/jekyll-scholar/issues/310> -->
  {%- capture citecount -%}
  {% bibliography_count -f papers -q @*[year={{y}}]* %}
  {%- endcapture -%}

  <!-- Only show citations for this year in the loop if any exist -->
  {% if citecount != "0"  %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f papers -q @*[year={{y}}]* %}
  {% endif %}
{% endfor %}

</div>
