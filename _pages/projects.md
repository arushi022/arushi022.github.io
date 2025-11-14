---
layout: page
title: Projects
permalink: /projects/
description:
nav: true
nav_order: 3
display_categories: [school, ai, personal, work, community]
horizontal: false
---

<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  {%- for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>

    {%- assign categorized_projects = site.projects | where: "category", category -%}
    {%- assign sorted_projects = categorized_projects | sort: "importance" -%}

    <div class="grid">
      <div class="grid-sizer"></div>
      {%- for project in sorted_projects -%}
        {% include projects_horizontal.html project=project %}
      {%- endfor -%}
    </div>

  {%- endfor %}
{%- else %}
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <div class="grid">
    <div class="grid-sizer"></div>
    {%- for project in sorted_projects -%}
      {% include projects.html project=project %}
    {%- endfor -%}
  </div>
{%- endif %}
</div>
