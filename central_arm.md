---
title: Central Arms
layout: default
---



#### Overview



#### Getting CNT variables

For most central arm track variables, one can get the variables in two ways:
from `PHCentralTrack` and from `PHSnglCentralTrack`.  The data are guaranteed
to be identical, except in the highly unlikely event somebody forgot to implement a method from `PHSnglCentralTrack`
into `PHCentralTrack`, which will fail in a safe way (you get a nan, a -9999, or a compiler error).

Here's a code snippet in to illustrate the two ways to get the momentum of the track.

```c++
  PHCentralTrack* ctrk = getClass<PHCentralTrack>(topNode,"PHCentralTrack");
  for ( unsigned int itrk = 0; itrk < ctrk->get_npart(); ++itrk )
    {
      PHSnglCentralTrack* strk = ctrk->get_track(itrk);
      float momentum = -9999;
      mom = strk->get_mom();
      mom = ctrk->get_mom(itrk);
    }
```



#### Links to internal PHENIX pages

[Information from the momentum reconstruction](https://www.phenix.bnl.gov/WWW/offline/wikioff/index.php/Information_from_the_momentum_reconstruction)

[Projections of the reconstructed tracks](https://www.phenix.bnl.gov/WWW/offline/wikioff/index.php/Projections_of_the_reconstructed_tracks)

[EMCal information on clusters](https://www.phenix.bnl.gov/WWW/offline/wikioff/index.php/EMCal_information_on_clusters)

[RICH information on PMT hits](https://www.phenix.bnl.gov/WWW/offline/wikioff/index.php/RICH_information_on_PMT_hits)

[Variables regarding particle ID using the high resolution TOF (WARNING THIS IS HIGHLY INCOMPLETE AND OUTDATED)](https://www.phenix.bnl.gov/WWW/offline/wikioff/index.php/Variables_regarding_particle_ID_using_the_high_resolution_TOF)

[Aerogel information](https://www.phenix.bnl.gov/WWW/offline/wikioff/index.php/Aerogel_information)



#### Papers

[Event Reconstruction in the PHENIX Central Arm Spectrometers, NIM A 482 (2002)](https://arxiv.org/abs/nucl-ex/0201013)





