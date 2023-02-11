---
layout: default
title: Rapport redirect_from
---


{% for post in site.posts %}
  {% if post.redirect_from %}
    {{ post.url }} redirected_from {{ post.redirect_from }}   
  {% endif %}
{% endfor %}
