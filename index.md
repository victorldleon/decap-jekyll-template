---
title: Index Page
layout: default
page_content:
    - internalName: Hero
      contentType: hero
      heading: Heading text
      text: hero
    - internalName: Speakers section
      contentType: speakers
      heading: speakers section title
      text: speakers section text
pageContent:
    - internalName: Hero Section - Index
      contentType: hero
      heading: Heading for Hero Section at index
      text: Text for hero section at index
    - internalName: Conferences section - Index
      contentType: conferences
      heading: Heading for conferences section at index
      text: Text for conferences section at index
---

hola
{% for item in page.page_content %}
{{ item.contentType }}
{% endfor %}
adios
