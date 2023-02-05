---
layout: default
title: test 2. test for nested arrays
date: 2022-12-31
update: 2023-02-01
permalink: /Tests/test2/
---


{%- assign allPostDates = "" | split: ',' -%}
{%- for post in site.posts %}
  {% assign postDate = post.update | default: post.date %}
  {%- assign allPostDates = allPostDates | push: postDate -%}
{%- endfor %}
{%- assign allPostDate = allPostDates | uniq | sort -%}


{{ allPostDate }}

{%- assign allPosts = "" | split: ',' -%}
{%- for date in allPostDate | order %}
  {% assign allNonUpdatedPosts = site.posts | where: "date",date %}
  {%- assign allPosts = allPosts | concat: allNonUpdatedPosts -%}
  {% assign allUpdatedPosts = site.posts | where: "update",date %}
  {% for updatedPost in allNonUpdatedPosts %}
    {% assign postFounded = allPosts | where: "path", post.path %}
    {% if postFounded %}
    {% else %}
      {%- assign allPosts = allPosts | concat: updatedPost -%}
    {% endif %}
  {%- endfor %}
{% endfor %}

{% for post in allPosts %}
  {{ post.update | default: post.date }} / {{ post.title }}
{% endfor %} 
