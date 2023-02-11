---
layout: default
title: Rapport vidéos mentionnées dans post mais non trouvées
---
{% assign staticUrlList = "" | split: "," %}
{% for file in site.static_files %}
  {% assign staticUrlList = staticUrlList | push: file.path %}
{% endfor %}

{% for post in site.posts %}
  {% if post.videos %}
## {{post.title}} / {{ post.url }}
  {% for video in post.videos %}
    {% if staticUrlList contains video.url %}
      ✅ vidéo {{video.url}} is referenced in {{post.url }}  and can be found
    {% else %}
      ❌ vidéo {{video.url}} is referenced in {{post.url }}  but cannot be found
    {% endif %}
  {% endfor %}
 {% endif %}
{% endfor %}

