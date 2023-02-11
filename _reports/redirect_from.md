---
title: Rapport redirect_from
---


{% for post in site.posts %}
  {% if post.redirect_from %}
## {{ post.title }} / {{ post.url }}
❎redirect_from {{ post.redirect_from }}   
  {% endif %}
{% endfor %}
