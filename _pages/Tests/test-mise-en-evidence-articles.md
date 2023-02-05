---
layout: default
title: Test mise en évidence articles
description: page d´accueil du blog de Marcos Ickx
permalink: /Tests/test3/
---
{% assign limite-epingles = 2 %}
{% assign epingles = site.posts | where: "epingle" %}
{% assign epingles = epingle | sort: "epingle" %}
{% if (epingles) %}
# Epinglés
  {% for epingle in epingles limit: limite-epingles %}
    <div class="epingle">
      <div class="epingle-image">
        ![{{epingle.image.alt}}]({{epingle.image.url}} "{{epingle.image.title}}")
      </div>
      <div class="epingle-post">
        [{{epingle.title}}][{{epingle.url}}]
        
        {{ epingle.excerpt }}   
      </div>
    </div>
{% endfor %}

{%- include posts.html limit=10 -%}

# Archives

{%- include archives.html debug=false -%}
Give feedback
