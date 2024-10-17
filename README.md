# Aquarius Particle Tagging Data

https://github.com/nthu-ga/aquarius-halos

This repository contains a description of the datasets presented in Pu et al. (2024):

- The Aquarius suite of 6 high-resolution stellar halos made with the STINGS particle tagging technique. These data can be downloaded from [https://doi.org/10.5281/zenodo.13888986](https://doi.org/10.5281/zenodo.13888986)
- A python script to convert the [Bullock & Johnston (2005)](http://adsabs.harvard.edu/abs/2005ApJ...635..931B) stellar halo models to the same format as the Aquarius data;
- Lists of particle progenitor IDs for the Auriuga L3 and L4 simulations; note that these are slightly different from those provided as part of the Auriga data release and described in [Grand et al. 2024](https://ui.adsabs.harvard.edu/abs/2024MNRAS.532.1814G). These data can be downloaded from [https://doi.org/10.5281/zenodo.13943963](https://doi.org/10.5281/zenodo.13943963).

Please cite some combination of the following references, as appropriate:
- Pu et al. (2024) for this repository and the Aquarius data (a link to this webpage and/or the Zenodo DOI for the Aquarius data is appreciated)
- [Cooper et al. (2010)](http://adsabs.harvard.edu/abs/2010MNRAS.406..744C) for the Aquarius models themselves (in addition to Pu et al.);
- [Cooper et al. (2017)](https://ui.adsabs.harvard.edu/abs/2017MNRAS.469.1691C) for the most complete description of the STINGS particle tagging methodology;

The Bullock & Johnston (2005) and Auriga data are available elsewhere as described below. 

## Aquarius

The Aquarius models from [Cooper et al. (2010)](http://adsabs.harvard.edu/abs/2010MNRAS.406..744C) can be downloaded from the following URL:

[https://doi.org/10.5281/zenodo.13888986](https://doi.org/10.5281/zenodo.13888986)

The public data, as described in the appendix of Pu et al. (2024), has the following structure:

```
 _ Header
|_ PartType0
    |_ Coordinates
    |_ LastTreeIndex
    |_ Mass
    |_ ParticleIDs
    |_ SubgroupNr
    |_ Velocities
|_ PartType1    
    |_ Coordinates    
    |_ LastTreeIndex    
    |_ Mass
    |_ ParticleIDs
    |_ SubgroupNr
    |_ Velocities
```


## Bullock & Johnston (2005)

The models described in [Bullock & Johnston (2005)](http://adsabs.harvard.edu/abs/2005ApJ...635..931B) can be downloaded from the following URL:

[http://user.astro.columbia.edu/~kvj/halos/](http://user.astro.columbia.edu/~kvj/halos/)

We provide a python script that, when run on the models available from the URL above, convert those data to HDF5 format with the same data model as the Aquarius data we provide. This script requires the python package [h5py](https://docs.h5py.org/en/stable/index.html).

To run the scipt, simply use the following command, passing one of the BJ05 data files and choosing a name for the HDF5 output:

`python Covert_BJ2Aq.py BJhalofile.dat outputname.hdf5`

We note that additional data on the BJ05 models are available as part of the Galaxia code:

https://galaxia.sourceforge.net/

## Auriga

As described in [Grand et al. 2024](https://ui.adsabs.harvard.edu/abs/2024MNRAS.532.1814G), the Auriga particle data can be downloaded from the following URL:

https://wwwmpa.mpa-garching.mpg.de/auriga

Note that Pu et al. 2024 work with a slightly different set of TreeID instead of those provided by the public data release of the Auriga project. We provide HDF5 files of our TreeID and the ParticleIDs for reference, which can be downloaded from the following URL:

https://doi.org/10.5281/zenodo.13943963

Although only the level 4 Auriga data were used in Pu et al. 2024, we also provide level 3 progenitor ID lists. Each file has the following structure, with datasets corresponding to each Auriga halo:

```
 _ halo_X
    |_ ParticleIDs
    |_ TreeID
```

Note that only halo 6, 16, 21, 23, 24, 27 are available in level 3.
