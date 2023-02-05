---
layout: default
title: Test mise en évidence articles
description: page d´accueil du blog de Marcos Ickx
permalink: /Tests/test3/
---
{% assign limite-epingles = 2 %}
{% assign epingles = site.posts | where: "epingle", 1 %}
{% if epingles %}
  {% assign epingles = epingles | sort: "epingle"  %}
<h1>Epinglés</h1>
  {% for epingle in epingles limit: limite-epingles %}
<div class="epingle">
<div class="epingle-image" style="display:float">
<img src="{{epingle.image.url}}" />
</div>
<div class="epingle-post">
<a href="{{epingle.url}}" title="{{epingle.title}}">{{epingle.title}}</a> 
<br />
{{ epingle.excerpt }}
</div>
</div>
  {% endfor %}
{% endif %}

{%- include posts.html limit=10 -%}

<h1>Archives</h1>

{%- include archives.html debug=false -%}
Give feedback
