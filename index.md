---
title: Index Page
layout: default
page_content:
  - internalName: Conferences section - Index
    contentType: conferences
    heading: Heading for conferences section at index
    text: Text for conferences section at index
  - internalName: Hero Section - Index
    contentType: hero
    heading: Heading for Hero Section at index
    text: Text for hero section at index
  - contentType: speakers
    internalName: Speakers Section - Index
    heading: Heading of Speakers section at index
    text: Text of Speakers section at index
  - contentType: themes
    heading: Heading themes section - index
    text: text themes section - index
    internalName: Themes Section - Index
---

{% for item in page.page_content %}
{% case item.contentType %}
{% when 'hero' %}
{% include hero.html %}
{% when 'speakers' %}
{% include speakers.html %}
{% when 'conferences' %}
{% include conferences.html %}
{% when 'themes' %}
{% include themes.html %}
{% endcase %}
{% endfor %}
