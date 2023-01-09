---
layout: default
---

{% assign posts = site.posts | where_exp: "post", "page.year = post.date | date: '%Y'" %}
{% if {{ posts | size }} > 0 %}
# {{page.year}}
{% for post in posts %}

## {{post.title}} 
{{ post.date | date "%d/%m/%Y" }} by {{post.author}}

{% endfor %}
{% endif %}
