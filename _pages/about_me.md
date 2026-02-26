---
layout: about
nav: false
dropdown: false
permalink: /about_me/
hide_header: false
subtitle:

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false

social: false
current: false
news: false
selected_papers: false
---

{% assign intro = site.bio | where: "introduction", true | first %}

{{ intro.content | markdown | remove: '<p>' | remove: '</p>' }}

{% include resume.html %}
