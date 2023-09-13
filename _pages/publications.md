---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2024, 2023, 2022, 2021, 2020, 2019]
nav: true
---
<!-- _pages/publications.md -->
<div class="publications">

<a href="https://scholar.google.com/citations?user=8LqmCjAAAAAJ">Google Scholar Profile</a>

{%- for y in page.years %}
  <h2 class="year" style="color: coral">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
