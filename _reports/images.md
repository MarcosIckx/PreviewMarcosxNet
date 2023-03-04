---
title: Rapport images mentionnées dans post mais non trouvées
---
{% assign staticUrlList = "" | split: "," %}
{% for file in site.static_files %}
  {% assign staticUrlList = staticUrlList | push: file.path %}
{% endfor %}

{% for post in site.posts %}
  {% if post.images %}
## {{ post.title }} / {{ post.url }}
  {% for image in post.images %}
### {{ image }} 
first : {{image.first}}
first.first : {{image.first.first}}
last : {{image.last}}

    {% if staticUrlList contains image.url %}
      ✅ image {{image.url}} is referenced in {{post.url }}  and can be found
    {% else %}
      ❌ image {{image.url}} is referenced in {{post.url }}  but cannot be found
    {% endif %}
  {% endfor %}
 {% endif %}
{% endfor %}
