---
layout: default
title: Rapport vidéos mentionnées dans post mais non trouvées
---


{% for post in site.posts %}
  {% if post.videos %}
## {{post.title}} / {{ post.url }}
  {% for video in post.videos %}
    {% if site.static_files contains video %}
      ✅ vidéo {{video.url}} is referenced in {{post.url }}  and can be found
    {% else %}
      ❌ vidéo {{video.url}} is referenced in {{post.url }}  but cannot be found
    {% endif %}
  {% endfor %}
 {% endif %}
{% endfor %}

