---
layout: default
title: test 2. test for nested arrays
date: 2022-12-31
update: 2023-02-01
permalink: /Tests/test2/
---


{%- assign allPostDates = "" | split: ',' -%}
{%- for post in site.posts %}
  {% assign postDate = post.update | default: post.date | date: "%s" %}
  {%- assign allPostDates = allPostDates | push: postDate -%}
{%- endfor %}
{%- assign allPostDates = allPostDates | uniq | sort | reverse -%}

{{ allPostDates }}

{% assign allPosts = "" | split: ',' %}
{% for date in allPostDates %}
  {% for post in site.posts %}
    {% assign postDate = post.update | default: post.date | date: "%s" %}
    {{ post.update }} ~ {{ post.date }} =  {{ postDate }} 
    to compare with {{ date }} 
    {% if (postDate == date) %} 
      {% assign allPosts = allPosts | push: post %}
      {{ post.url}}  added in the allPosts (now size={{ allPosts.size }})
    {% endif %} 
  {% endfor %}
{% endfor %}

{% for post in allPosts %}
  {{ post.update | default: post.date }} / {{ post.title }}
{% endfor %} 
