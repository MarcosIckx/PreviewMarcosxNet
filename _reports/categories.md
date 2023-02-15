---
title: liste des catégories et des entries par categorie
---

{%- assign allTaxonomyNames = "" | split: ',' -%}
{%- for taxonomy in site.categories %}
{%- assign allTaxonomyNames = allTaxonomyNames | push: taxonomy[0] -%}
{%- endfor %}
{%- assign allTaxonomyNames = allTaxonomyNames | uniq | sort_natural -%}

{% include taxonomy/entriesPerTaxonomy.html taxonomyNameList=allTaxonomyNames taxonomyCollection=site.categories %}
