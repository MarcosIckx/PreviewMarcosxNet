---
layout: default
title: Rapport vidéos mentionnées dans post mais non trouvées
---

{% assign videoList = "" | split: "," %}
{% for post in site.posts %}
    {% for video in post.videos %}
      {% if site.static_files contains video %}
        ✅ vidéo {{video.url}} is referenced in {{post.url }}  and can be found
      {% else %}
        ❌ vidéo {{video.url}} is referenced in {{post.url }}  but cannot be found
  {% endif %}
    {% endfor %}
  {% endif %}
{% endfor %}

{% for video in videoList  %}
  {% if site.static_files contains video %}
  {% else %}
    vidéo {{video.url}} is referenced in a post but cannot be found
  {% endif %}
{% endfor %}
