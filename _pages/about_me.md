---
layout: page
title: about me
nav: false
dropdown: false
permalink: /about_me/
introduction: true
subtitle:
---

{% include resume.html %}

{{ intro.content | markdown | remove: '<p>' | remove: '</p>' }}