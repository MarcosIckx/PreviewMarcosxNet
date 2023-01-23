---
layout: default
title: Liste des vidéos
description: Page qui référence toutes les vidéos 
permalink: /videos/liste.html
---

{% for file in site.static_files %}
  
  ### {{ file.path }}
  
  ### {{ file.extension }}
  
  {{ file }}
  
  {% if file.extension contains ".mp4" %}
    # {{ file.basename }}
    file: {{ file }}
    Video.url : {{ file.path }}
    Video.id : {{ file.basename }}
    Video.type : {{ file.extension }}
    Video.alt : ---
  {% endif %}
{% endfor %}
