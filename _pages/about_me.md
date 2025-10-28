---
layout: page
title: about me
nav: false
dropdown: false
permalink: /about_me/
subtitle:
---

{% assign intro = site.bio | where: "introduction", true | first %}

{{ intro.content | markdown | remove: '<p>' | remove: '</p>' }}