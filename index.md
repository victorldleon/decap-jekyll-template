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
---

hola
{% for item in page.page_content %}
{{ item.contentType }}
{% endfor %}
adios
