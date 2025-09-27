---
layout: page
title: research
permalink: /research/
nav: true
nav_order: 3
display_categories: [research]
horizontal: false
---

<!-- pages/research.md -->
<div class="projects">
{% for category in page.display_categories %}

{% assign categorized_projects = site.projects | where: "category", category %}

  <h3 class="category">Current</h3>
  {% assign current_projects = categorized_projects | where: "status", "current" | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in current_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>

  <h3 class="category">Archive</h3>
  {% assign archived_projects = categorized_projects | where: "status", "archive" | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in archived_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>

  <h3 class="category">On the Horizon</h3>
  {% assign future_projects = categorized_projects | where: "status", "future" | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in future_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
{% endfor %}
</div>
