---
layout: page
permalink: /bio/
title: bio
description:
nav: false
nav_order: 6
---

{% assign sorted_bio_entries = site.bio | sort: "order" %}
{% for qa_brief in sorted_bio_entries %}
  {% include qa_brief.html
    url=qa_brief.url
    topic=qa_brief.topic
    content=qa_brief.content
    redirect=qa_brief.redirect
    inline=qa_brief.inline
   %}
{% endfor %}