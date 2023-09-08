---
title: Title for the index page
layout: default
content:
  - include:
      internalName: Index hero
      contentType: hero
      heading: Index hero heading
      text: Index hero text
  - include:
      internalName: Speakers Home
      contentType: speakers
      heading: Speakers title home
      text: speakers title home
  - include:
      internalName: Index - Conferences list
      contentType: conferences
      heading: Conferences list
      text: Index conferences list text
---

{% include navigation.html %}
{% for item in page.content %}
    {% if item.include.contentType == "hero" %}
        {% include hero.html %}
    {% endif %}
{% endfor %}
<div class="container">
    {% for item in page.content %}
        {% if item.include.contentType == "speakers" %}
            {% include speakers.html  %}
        {% elsif item.include.contentType == "conferences" %}
            {% include conferences.html  %}
        {% elsif item.include.contentType == "media" %}
            {% include media.html  %}
        {% endif %}
    {% endfor %}
</div> 