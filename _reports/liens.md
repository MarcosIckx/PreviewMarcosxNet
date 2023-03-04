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
## <a href="{{ post.url }}">{{ post.url }}</a>
  {% for link in links %}
    {% assign linkUrl = link.last.url | default: link.url %}
    {% assign firstPartOfUrl = linkUrl | split:"/" | first %}
    {% if firstPartOfUrl == ""  %}
      {% if postUrlList contains linkUrl %}
✅ valid link : 
      {% else %}
❌ invalid link :
      {% endif %}
<a href="{{ linkUrl }}">{{ linkUrl }}</a> 
    {% else %}
<a href="{{ linkUrl }}">{{ linkUrl }}</a> is external to our website so must be manually checked.
    {% endif %}
  {% endfor %}
 {% endif %}
{% endfor %}
