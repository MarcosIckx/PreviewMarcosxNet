---
layout: default
title: Liste des vidéos
description: Page qui référence toutes les vidéos 
permalink: /videos/liste.html
---

{% for file in site.static_files %}
  
# {{ file.basename }}
  
{{ file.path}} |{{ file.basename }} |{{ file.extname }}
  

{% assign extension = file.extname | downcase %}
{% if extension contains ".mp4" %}
    
## Video {{ file.basename }}
    
file: {{ file }}
Video.url : {{ file.path }}
Video.id : {{ file.basename }}
Video.type : {{ file.extension }}
Video.alt : ---
  
{% endif %}

{% endfor %}
