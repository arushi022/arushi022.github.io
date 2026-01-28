---
layout: about
title: about
permalink: /
subtitle:

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

current: true   # includes current reading/workings/recipes 
news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page

current_items:
  - title: "Reading:"
    body: "Pachinko by Min Jin Lee"
    url: "https://www.goodreads.com/book/show/34051011-pachinko"
  - title: "Listening to:"
    body: "Humans of Bombay Podcast"
    url: "https://open.spotify.com/show/5wHwtGp4PV0hcSBdLZP7V3?si=27a1eb2d6beb401e"
  - title: "Cooking experiments:"
    body: "Mango rasmalai cake for Diwali"
    url: "https://www.instagram.com/arushi_bakes/"
---

{% assign intro = site.bio | where: "introduction", true | first %}

{{ intro.content | markdown | remove: '<p>' | remove: '</p>' }}