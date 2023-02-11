---
layout: default
title: Rapport redirect_from &amp; redirect_to
---
{% for post in site.posts %}
  {% if post.redirect_from %}
    {{ post.url }} redirected_ from {{ post.redirect_from }}
    
    
  {% endif %}
{% endfor %}
