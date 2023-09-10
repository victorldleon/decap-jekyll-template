---
layout: default
title: Index Page
content:
  - internalName: hero
    contentType: hero
    heading: Welcome to Our Conference
    text: We are glad to have you here.
  - internalName: speakers
    contentType: speakers
    heading: Meet Our Speakers
    text: Here are some of our notable speakers.
---

{% for content in page.content %}
  {% include {{ content.contentType | default: "default" }}.html %}
{% endfor %}
