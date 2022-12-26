---
layout: page
permalink: /research/
title: Research
description: I have participated in the research and development of EU-funded projects, such as COLA, during my postdoctoral research experience. MiCADO, the output of the COLA project, is open-source and a highly customisable multi-cloud orchestration and auto-scaling framework for Docker containers orchestrated by Kubernetes. Furthermore, I have joined the RABBDA project, a research collaboration between the UoW and Westminster International University in Tashkent (WIUT), which aims to reduce access barriers to big data analytics tools. I have co-authored research articles in high-quality journals and conference proceedings. I am an active reviewer in IEEE Transactions in Cloud Computing, Journal of Grid Computing and the Journal of Cloud Computing, as well as other conferences.
years: [2020, 2019, 2018, 2017, 2016]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
