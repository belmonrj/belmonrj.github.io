---
title: TOFE
layout: default
---



#### TOFE overview

{{ site.data.tofe.info.intro }}
<br>
<br>
{{ site.data.tofe.info.slat }}
<br>
<br>
{{ site.data.tofe.info.system }}



#### TOFE analysis variables

These "get" methods give access to the TOFE variables used for analysis.
The variable type, name of the get method, and a brief description are given below.

  Type  |  Name  |  Description   <br>
 ------ | ------ | -------------
{% for var in site.data.tofe.vars %}
   {%- assign print_type = var.type -%}
   {%- assign print_name = var.name -%}
   {%- assign print_desc = var.desc -%}
   {%- assign print_me = print_type | append: ' | ' | append: print_name | append: ' | ' | append: print_desc %}
   {{ print_me }}
{%- endfor -%}
{{ nil }}



#### C++ code from `PHCentralTrack.h` and/or `PHSnglCentralTrack.h`


```c++
{% for var in site.data.tofe.vars %}
   {{ var.code }}
{%- endfor -%}
{{ nil }}
{{ nil }}
```


