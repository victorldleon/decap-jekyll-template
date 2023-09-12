---
title: Index Page
layout: default
page_content:
  - internalName: Media Section - Index
    contentType: media
    heading: "Media Section "
    text: "Media Section "
  - internalName: Hero Section - Index
    contentType: hero
    heading: Heading for Hero Section at index
    text: Text for hero section at index
  - internalName: Conferences section - Index
    contentType: conferences
    heading: Heading for conferences section at index
    text: Text for conferences section at index
  - internalName: Speakers Section - Index
    contentType: speakers
    heading: Heading of Speakers section at index
    text: Text of Speakers section at index
  - internalName: Speakers Section - Index - bottom
    contentType: speakers
    heading: "-"
    text: "-"
---

{% for item in page.page_content %}
{% case item.contentType %}
{% when 'hero' %}

{% include hero.html %}

<main class="homepage">
{% when 'speakers' %}
{% include speakers.html %}
{% when 'conferences' %}
{% include conferences.html %}
{% when 'media' %}
{% include media.html %}

</main>
{% endcase %}

{% endfor %}
