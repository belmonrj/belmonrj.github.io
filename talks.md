---
title: Talks
layout: default
---



### Talks



{% for var in site.data.talks.vars %}
   {%- assign print_title = var.title -%}
   {%- assign print_venue = var.venue -%}
   {%- assign print_date = var.date -%}
   {%- assign print_file = var.file -%}
   {%- assign print_me = '- ' | append: print_title | append: ' <br> ' | append: print_venue | append: ', ' | append: print_date | append: ', ' | append: print_file | append: ' <br><br> ' %}
   {{ print_me }}
{%- endfor -%}
{{ nil }}


