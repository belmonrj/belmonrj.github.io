---
title: TOFW
layout: default
---

### TOFW overview

The TOFW is a time-of-flight (TOF) detector in the west (W) arm of the PHENIX central spectrometer.
It was designed, developed, and assembled at Vanderbilt University with Julia Velkovska as the project lead.

The individual component of the TOFW detector is the mult-gap resistive plate chamber (MRPC).
Each MRPC has six 230 micron gaps separated by glass plates.  The gaps are filled with a gas mixture.
During the commissioning run in 2007 (Run7), the gas mixture was
95% R134a (1,1,1,2-Tetrafluoroethane) and
5% isobutane (2-Methylpropane).
In the 2008 operational period (Run8) the gas mixture
was changed to 95% R134a, 4.5% isobutane, and
0.5% sulfur hexafluoride (SF6).
Starting in the operational period in 2011 (Run11),
The gas mixture was changed to 92% R134a, 5% isobutane,
and 3% SF6.
At either side (longitudinally) of the
gaps are electrodes held at +/- 7 kV for a total potential difference of 14 kV across the gaps.
Outside of the electrodes on either side (longitudinally) are sets of four copper strips that are
read out on either side, for a total of 8 readout channels per MRPC.
When charged particles cross the gap, the gas is ionized.  The charge in the gas is imaged in the strips.
The induced charge in the strips is read out on either end (transversely).  Each strip is about 37 cm
long and 2.8 cm wide.  The lengthwise location of the hit in the strip is determined via the difference in time
on either end.  Since the strip is only 1 inch wide, the widthwise location of the hit is taken to be the center
of the strip.

The TOFW system consists of four boxes.  Each box subtends 11.5 degrees in azimuth and 0.35 units in pseudorapidity.
There are two boxes in sector 1 and two boxes in sector 2, with each sector receiving full coverage in pseudorapidity
and half coverage in azimuth.
Each box has four high voltage busses in two rows.  Each high voltage buss powers 8 MRPCs, for a total of 32 per box
and 128 total, meaning there are 1024 readout channels in total.





### Analysis variable summary

The variables needed for analysis are accessible via "get" methods in the `PHCentralTrack` class.

The table below shows all available methods, the return type, and a description of the quantity.


#### Table

|  Type     |     Name           | Description                                                                                                         |
| --------- | ------------------ | ------------------------------------------------------------------------------------------------------------------- |
|  short    |     get_tofwid     | Ron needs to double check                                                                                           |
|  float    |     get_ptofwx     | x-component of the projection of the cgl track onto the TOFW                                                        |
|  float    |     get_ptofwy     | y-component of the projection of the cgl track onto the TOFW                                                        |
|  float    |     get_ptofwz     | z-component of the projection of the cgl track onto the TOFW                                                        |
|  float    |     get_pltofw     | pathlength of the track from the collision to the TOFW                                                              |
|  float    |     get_tofwdphi   | difference between track projection and the track hit in the phi direction (viz dphi means delta phi)               |
|  float    |     get_tofwdz     | difference between track projection and the track hit in the z direction (viz dz means delta z)                     |
|  float    |     get_stofwdphi  | difference between track projection and the swapped track hit in the phi direction (viz dphi means delta phi)       |
|  float    |     get_stofwdz    | difference between track projection and the swapped track hit in the z direction (viz dz means delta z)             |
|  int      |     get_striptofw  | the unique id number of the strip of the track hit                                                                  |
|  float    |     get_tofwx      | x-component of the TOFW track hit                                                                                   |
|  float    |     get_tofwy      | y-component of the TOFW track hit                                                                                   |
|  float    |     get_tofwz      | z-component of the TOFW track hit                                                                                   |
|  float    |     get_ttofw      | time of flight from the vertex to the TOFW (the BBC start time for the event is subtracted)                         |
|  float    |     get_qtofw      | the total charge (ADC) of the TOFW track hit                                                                        |
|  float    |     get_tofwadcup  | the charge (ADC) from the upper side of the TOFW track hit                                                          |
|  float    |     get_tofwadcdw  | the charge (ADC) from the lower side of the TOFW track hit                                                          |
|  float    |     get_tofwtdcup  | the raw time (TDC) from the upper side of the TOFW track hit                                                        |
|  float    |     get_tofwtdcdw  | the raw time (TDC) from the lower side of the TOFW track hit                                                        |
|  float    |     get_tofwsdz    | the sigmalized version of tofwdz                                                                                    |
|  float    |     get_tofwsdphi  | the sigmalized version of tofwdphi                                                                                  |
|  float    |     get_stofwsdphi | the sigmalized version of stofwdz                                                                                   |
|  float    |     get_stofwsdz   | the sigmalized version of stofwdphi                                                                                 |
|  float    |     get_m2tofw     | the calculated mass squared of the TOFW track (using ttofw, pltofw, and mom)                                        |
|  int      |     get_idtrk_tofw | Ron needs to double check                                                                                           |

#### C++ code


From `PHCentralTrack.h`

```c++
  virtual short get_tofwid     (const unsigned int itrk) const;
  virtual float get_ptofwx     (const unsigned int itrk) const;
  virtual float get_ptofwy     (const unsigned int itrk) const;
  virtual float get_ptofwz     (const unsigned int itrk) const;
  virtual float get_pltofw     (const unsigned int itrk) const;
  virtual float get_tofwdphi   (const unsigned int itrk) const;
  virtual float get_tofwdz     (const unsigned int itrk) const;
  virtual float get_stofwdphi  (const unsigned int itrk) const;
  virtual float get_stofwdz    (const unsigned int itrk) const;
  virtual int   get_striptofw  (const unsigned int itrk) const;
  virtual float get_tofwx      (const unsigned int itrk) const;
  virtual float get_tofwy      (const unsigned int itrk) const;
  virtual float get_tofwz      (const unsigned int itrk) const;
  virtual float get_ttofw      (const unsigned int itrk) const;
  virtual float get_qtofw      (const unsigned int itrk) const;
  virtual float get_tofwadcup  (const unsigned int itrk) const;
  virtual float get_tofwadcdw  (const unsigned int itrk) const;
  virtual float get_tofwtdcup  (const unsigned int itrk) const;
  virtual float get_tofwtdcdw  (const unsigned int itrk) const;
  virtual float get_tofwsdz    (const unsigned int itrk) const;
  virtual float get_tofwsdphi  (const unsigned int itrk) const;
  virtual float get_stofwsdphi (const unsigned int itrk) const;
  virtual float get_stofwsdz   (const unsigned int itrk) const;
  virtual float get_m2tofw     (const unsigned int itrk) const;
  virtual int   get_idtrk_tofw (const unsigned int itrk) const;
```
