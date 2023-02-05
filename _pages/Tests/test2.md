---
layout: default
title: test 2. test for nested arrays
date: 2022-12-31
update: 2023-02-01
---

page before : {{ page | inspect }}

{% assign sort_date = page.update | default: page.date %}

sort date : {{ sort_date | inspect }}

{% assign page = page | push: sort_date %}


page after : {{ page | inspect }}


