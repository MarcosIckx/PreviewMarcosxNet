---
layout: default
---

# {{page.year}}
{%- for post in site.posts -%}
{%- assign yearOfPost = post.date | date: "%Y" -%}
{%- if yearOfPost == page.year %}
## {{post.title}} 
{{ post.date | date "%d/%m/%Y" }} by {{post.author}}
{%- endif -%}
{%- endfor -%}

