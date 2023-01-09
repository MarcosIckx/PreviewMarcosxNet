---
layout: default:
---

{% assign posts = site.posts | where_exp: "post", "post.date | date '%Y' = page.year" %}
{% if posts.size > 0 %}
# {{page.year}}
{% for post in posts %}

## {{post.title}} 
{{ post.date | date "%d/%m/%Y" }} by {{post.author}}

{% endfor %}
{% endif %}
