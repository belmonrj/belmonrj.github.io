---
title: TOFW
layout: default
---



#### TOFW overview

{{ site.data.tofw.info.intro }}
<br>
<br>
{{ site.data.tofw.info.mrpc }}
<br>
<br>
{{ site.data.tofw.info.system }}



#### TOFW analysis variables

These "get" methods give access to the TOFW variables used for analysis.
The variable type, name of the get method, and a brief description are given below.

  Type  |  Name  |  Description   <br>
 ------ | ------ | -------------
{% for var in site.data.tofw.vars %}
   {%- assign print_type = var.type -%}
   {%- assign print_name = var.name -%}
   {%- assign print_desc = var.desc -%}
   {%- assign print_me = print_type | append: ' | ' | append: print_name | append: ' | ' | append: print_desc %}
   {{ print_me }}
{%- endfor -%}
{{ nil }}



#### C++ code from `PHCentralTrack.h`


```c++
{% for var in site.data.tofw.vars %}
   {{ var.code }}
{%- endfor -%}
{{ nil }}
{{ nil }}
```


