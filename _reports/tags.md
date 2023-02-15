---
title: liste des tags et des entries par Tag
---

{%- assign allTaxonomyNames = "" | split: ',' -%}
{%- for taxonomy in site.tags %}
{%- assign allTaxonomyNames = allTaxonomyNames | push: taxonomy[0] -%}
{%- endfor %}
{%- assign allTaxonomyNames = allTaxonomyNames | uniq | sort_natural -%}

{% include taxonomy/entriesPerTaxonomy.html taxonomyNameList=allTaxonomyNames taxonomyCollection=site.tags %}
