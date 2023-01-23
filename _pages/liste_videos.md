---
layout: default
title: Liste des vidéos
description: Page qui référence toutes les vidéos 
permalink: /videos/liste.html
---

{% for file in site.static_files %}

{% assign extension = file.extname | downcase %}
{% if extension contains ".mp4" %}
    
## Video {{ file.basename }}

Video.url : {{ file.path }}

Video.id : {{ file.basename }}

Video.type : {{ file.extname }}

Video.alt : ---
  
{% endif %}

{% endfor %}
