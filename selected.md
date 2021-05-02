---
title: Selected Publications
layout: default
---



### Selected Publications



{% for var in site.data.publications.short %}
   {%- assign print_title = var.title -%}
   {%- assign short_doi = var.doi -%}
   {%- assign print_doi = '[' | append: short_doi | append: '](https://doi.org/' | append: short_doi | append: ')' -%}
   {%- assign short_arxiv = var.arxiv -%}
   {%- assign print_arxiv = '[arXiv:' | append: short_arxiv | append: '](https://arxiv.org/abs/' | append: short_arxiv | append: ')' -%}
   {%- assign short_inspire = var.inspire -%}
   {%- assign print_inspire = '[inspire:' | append: short_inspire | append: '](https://inspirehep.net/literature/' | append: short_inspire | append: ')' -%}
   {%- assign print_me = '- ' | append: print_title | append: ' <br> ' | append: print_doi | append: ', ' | append: print_arxiv | append: ', ' | append: print_inspire | append: ' <br><br> ' %}
   {{ print_me }}
{%- endfor -%}
{{ nil }}

