---
title: Rapport otherLinks
---
{% assign postUrlList = "" | split: "," %}
{% for post in site.posts %}
  {% assign postUrlList = postUrlList | push: post.url %}
{% endfor %}

{% for post in site.posts %}
  {% if post.otherLinks %}
## <a href="{{ post.url }}">{{ post.url }}</a>
    {% for link in post.otherLinks %}
      {% assign linkUrl = link.last.url | default: link.url  %}
      {% assign firstPartOfUrl = linkUrl | split:"/" | first %}
      {% if firstPartOfUrl == ""  %}
        {% if postUrlList contains linkUrl %}
✅ link found :
        {% else %}
❌ link not found : {% endif %}
<a href="{{ linkUrl }}">{{ linkUrl }}</a>
      {% else %}
<a href="{{ linkUrl }}">{{ linkUrl }}</a> 
is external to our website so must be manually checked.
      {% endif %}
    {% endfor %}
  {% endif %}
{% endfor %}
