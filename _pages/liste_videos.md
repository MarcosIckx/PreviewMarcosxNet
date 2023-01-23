---
layout: default
title: Liste des vidéos
description: Page qui référence toutes les vidéos 
permalink: /videos/liste.html
---

{%- for file in site.static_files -%}
  {% if file.extension contains ".mp4" %>
    Video.url : {{ file.path }}
    Video.id : {{file.}}
  {% endif %}
{% endfor %}
