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
  {% assign updatedPosts = site.posts | where: "update" | sort: "update" | reverse %}
  {% for post in updatedPosts %}
    {% assign postDate = post.update | date: "%s" %}
    {% if (postDate == date) %} 
      {% assign allPosts = allPosts | push: post %}
    {% elsif (postDate < date) %}
      {% break %}
    {% endif %} 
  {% endfor %}
  {% assign post = site.posts | where: "date" | sort: "date" | reverse %}
    {% if post.update %}
    {% else %}
      {% assign postDate = post.date | date: "%s" %}
      {% if (postDate == date) %} 
        {% assign allPosts = allPosts | push: post %}
      {% elsif (postDate < date) %}
        {% break %}
      {% endif %}     
    {% endif %} 
  {% endfor %}
{% endfor %}

{% for post in allPosts %}
  {{ post.update | default: post.date | date: "%Y-%m-%d" }} / {{ post.title }}
{% endfor %} 
