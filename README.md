# Aquarius Particle Tagging Data

https://github.com/nthu-ga/aquarius-halos

This repository contains a description of the datasets presented in Pu et al. (2024):

- The Aquarius suite of 6 high-resolution stellar halos made with the STINGS particle tagging technique. These data can be downloaded from https://doi.org/10.5281/zenodo.13888986
- A python script to convert the [Bullock & Johnston (2005)](http://adsabs.harvard.edu/abs/2005ApJ...635..931B) stellar halo models to the same format as the Aquarius data;
- Lists of particle progenitor IDs for the Auriuga L3 and L4 simulations; note that these are slightly different from those provided as part of the Auriga data release and described in [Grand et al. 2024](https://ui.adsabs.harvard.edu/abs/2024MNRAS.532.1814G).

Please cite some combination of the following references as appropriate:
- Pu et al. (2024) for this repository and the Aquarius data (a link to this webpage and/or the Zenodo DOI for the Aquarius data is appreciated)
- [Cooper et al. (2010)](http://adsabs.harvard.edu/abs/2010MNRAS.406..744C) for the Aquarius data (in addition to Pu et al.);
- [Cooper et al. (2017)](https://ui.adsabs.harvard.edu/abs/2017MNRAS.469.1691C) for the most complete description of the STINGS particle tagging methodology;

The Bullock & Johnston (2005) and Auriga data are avaialble elsewhere as described below. 

## Aquarius

## Bullock & Johnston (2005)

The models described in [Bullock & Johnston (2005)](http://adsabs.harvard.edu/abs/2005ApJ...635..931B) can be downloaded from the following URL:

http://user.astro.columbia.edu/~kvj/halos/

In this repository we provide a python script that, when run on the models available from the URL above, cover those data to HDF5 format with the same data model as the Aquarius data we provide.

`Example of runnning the code...`

We note that additional data on the BJ05 models are avialable as part of the the Galaxia code:

https://galaxia.sourceforge.net/

## Auriga

As described in [Grand et al. 2024](https://ui.adsabs.harvard.edu/abs/2024MNRAS.532.1814G), the Auriga particle data can be downloaded from the following URL:

https://wwwmpa.mpa-garching.mpg.de/auriga
