---
layout: page
permalink: /publications/
title: publications
description: My publications in reverse chronological order with highlights in <strong>bold</strong>.
years: [2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010, 2006]
order: 7
---

<h3 class="year">Preprints</h3>
{% bibliography -f preprints %}

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
