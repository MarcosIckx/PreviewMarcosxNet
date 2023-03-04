---
title: Rapport liens mentionnés dans post mais non trouvés
---
{% assign postUrlList = "" | split: "," %}
{% for post in site.posts %}
  {% assign postUrlList = postUrlList | push: post.url %}
{% endfor %}

{% for post in site.posts %}
  {% assign links = post.liens | default: post.links %}
  {% if links %}
## {{ post.title }} / {{ post.url }}
  {% for link in links %}
    {% assign linkUrl = link.last.url | default: link.url %}
    {% assign firstPartOfUrl = linkUrl | split:"/" | first %}
    {% if firstPartOfUrl == ""  %}
      {% assign lastPartOfUrl = linkUrl | split:"/" | last %}
      {% if lastPartOfUrl == ""  %}
      {% else %}
        ❌ relative url is not finishing by /. please take action to fix it.
      {% endif %}
      {% if postUrlList contains linkUrl %}
        ✅ link {{linkUrl}} is referenced in {{ post.url }}  and can be found
      {% else %}
        ❌ link {{linkUrl}} is referenced in {{ post.url }}  but cannot be found
      {% endif %}
    {% else %}
      [{{ linkUrl }}] is external to our website so must be manually checked.
    {% endif %}
  {% endfor %}
 {% endif %}
{% endfor %}
