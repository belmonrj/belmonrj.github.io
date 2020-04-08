---
title: TOFW
layout: default
---

### Variable summary

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

### C++ code

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
