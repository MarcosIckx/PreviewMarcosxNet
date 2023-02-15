---
title: liste des tags et des entries par Tag
---

{%- assign allTagNames = "" | split: ',' -%}
{%- for tag in site.tags %}
{%- assign allTagNames = allTagNames | push: tag[0] -%}
{%- endfor %}
{%- assign allTagNames = allTagNames | uniq | sort_natural -%}

{% include taxonomy/entriesPerTaxonomy.html taxonomyNameList=allTagNames taxonomyCollection=site.tags %}
