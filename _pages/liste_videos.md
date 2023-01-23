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
{% assign splittedPath = file.path | remove_first: "/" | split: '/' %}
{% if splittedPath[0] == "img" and splittedPath[1] == "posts" %}
video.date : {{ splittedPath[2] }}-{{ splittedPath[3] }}-{{ splittedPath[4] }}
{% endif %}

Video.id : {{ file.basename }}

Video.type : video/{{ file.extname | remove: "."}}

Video.alt : {{splittedPath[5] | replace: "-", " "}} : {{file.basename | replace: "-", " "}}
  
{% endif %}

{% endfor %}
