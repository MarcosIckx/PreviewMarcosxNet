---
title: Rapport otherLinks
---


{% for post in site.posts %}
  {% if post.otherLinks %}
## {{ post.url }}
    {% for link in post.otherLinks %}
### {{ link.title }}
      {% assign last = link.url | split "/" | last %}
compare {{ last }} 
      {% if last == "" %}
✅{{link.url}}
      {% elsif last contains "index.html" %}
❎{{link.url}}
      {% else %}
❌{{link.url}}
      {% endif %}
    {% endfor %}
  {% endif %}
{% endfor %}
