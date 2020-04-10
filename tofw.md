---
title: TOFW
layout: default
---

### TOFW overview

The TOFW is a time-of-flight (TOF) detector in the west (W) arm of the PHENIX central
spectrometer.  It was designed, developed, and assembled at Vanderbilt University with
Julia Velkovska as the project lead.

The individual component of the TOFW detector is the mult-gap resistive plate chamber
(MRPC).  Each MRPC has six 230 micron gaps separated by glass plates.  The gaps are filled
with a gas mixture.  During the commissioning run in 2007 (Run7), the gas mixture was 95%
R134a (1,1,1,2-Tetrafluoroethane) and 5% isobutane (2-Methylpropane).  In the 2008
operational period (Run8) the gas mixture was changed to 95% R134a, 4.5% isobutane, and
0.5% sulfur hexafluoride (SF6).  Starting in the operational period in 2011 (Run11), The
gas mixture was changed to 92% R134a, 5% isobutane, and 3% SF6.  At either side
(longitudinally) of the gaps are electrodes held at +/- 7 kV for a total potential
difference of 14 kV across the gaps.  Outside of the electrodes on either side
(longitudinally) are sets of four copper strips that are read out on either side, for a
total of 8 readout channels per MRPC.  When charged particles cross the gap, the gas is
ionized.  The charge in the gas is imaged in the strips.  The induced charge in the strips
is read out on either end (transversely).  Each strip is about 37 cm long and 2.8 cm wide.
The lengthwise location of the hit in the strip is determined via the difference in time
on either end.  Since the strip is only 1 inch wide, the widthwise location of the hit is
taken to be the center of the strip.

The TOFW system consists of four boxes.  Each box subtends 11.5 degrees in azimuth and
0.35 units in pseudorapidity.  There are two boxes in sector 1 and two boxes in sector 2,
with each sector receiving full coverage in pseudorapidity and half coverage in azimuth.
Each box has four high voltage busses in two rows.  Each high voltage buss powers 8 MRPCs,
for a total of 32 per box and 128 total, meaning there are 1024 readout channels in total.



### Trying liquid code with yaml data...

#### Trying C++ code...

From `PHCentralTrack.h`



```c++
{% for var in site.data.tofw.vars %}
   {{ var.code }}
{%- endfor -%}
{{ }}
```




#### Trying a table...




  Type  |  Name  |  Description
 ------ | ------ | -------------
{% for var in site.data.tofw.vars %}
   {%- assign print_type = var.type -%}
   {%- assign print_name = var.name -%}
   {%- assign print_desc = var.desc -%}
   {%- assign print_me = print_type | append: ' | ' | append: print_name | append: ' | ' | append: print_desc %}
   {{ print_me }}
{%- endfor -%}

