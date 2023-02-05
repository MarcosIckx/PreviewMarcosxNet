---
layout: default
title: test 2. test for nested arrays
date: 2022-12-31
update: 2023-02-01
permalink: /Tests/test2/
---

page before : {{ page }}

{% assign sort_date = page.update | default: page.date %}

sort date : {{ sort_date | jsonify }}

{% assign page = page | push: sort_date %}


page after : {{ page }}


