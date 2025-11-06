---
title: Jiutian GAEA-HBT Mock Catalogs
permalink: /gaea-hbt/
layout: work
---

## Overview

The mock catalogs presented here are introduced in the [GAEA mock paper](https://arxiv.org/abs/2511.03281). 

### Simulation Specifications

| Simulation    | Boxsize (Mpc/h) | Softening (kpc/h) | Particle Mass (M⊙/h) | Particles | Snapshots | Cosmology |
|---------------|-----------------|-------------------|----------------------|-----------|-----------|-----------|
| Jiutian-1G    | 1000            | 4.0               | 3.723 × 10^8         | 6144^3    | 128       | Planck 2018 (Ω_m=0.3111, h=0.6766) |
| Jiutian-2G    | 2000            | 7.0               | 2.978 × 10^9         | 6144^3    | 128       | Planck 2018 (Ω_m=0.3111, h=0.6766) |

### GAEA Model Parameters

Key differences of Jiutian-1G and 2G in SAM parameters used in the [GAEA model](https://sites.google.com/inaf.it/gaea/):

| Parameter | Meaning | Jiutian-1G | Jiutian-2G |
|-----------|---------|------------|------------|
| ε_reheat | Reheating efficiency | 0.5 | 0.7 |
| ε_eject | Ejection efficiency | 0.2 | 0.2 |
| γ_reinc | Reincorporation efficiency | 1.0 | 1.0 |
| κ_radio (×10⁻⁵) | Hot gas black hole accretion efficiency | 1.0 | 5.0 |
| f_BH | Cold gas accretion efficiency | 0.005 | 0.08 |
| ξ_slow | Ratio between specific angular momentum of gas cooling through "slow mode" and that of the halo | 1.4 | 1.0 |
| ξ_rapid | Ratio between specific angular momentum of gas cooling through "rapid mode" and that of the halo | 2.0 | 1.4 |

For more details on the SAM parameters, please refer to [Xie et al. 2020](https://arxiv.org/abs/2003.12757).

### Contact Information

- [Zhenlin Tan](mailto:zltan999@sjtu.edu.cn) (Shanghai Jiao Tong University)
- [Lizhi Xie](mailto:xielizhi1988@163.com) (Tianjin Normal University) 
- [Jiaxin Han](mailto:jiaxin.han@sjtu.edu.cn) (Shanghai Jiao Tong University)

## Data Access
We release three types of catalogs, including 

- [HBT+ subhalo snapshots]({{site.baseurl}}/download/primary/gaea-hbt/hbt/)
    
    Note the HBT+ subhalos contains merger trees in themselves, so that no separate tree files are needed for linking them across snapshots. See the [HBT+ wiki](https://github.com/Kambrian/HBTplus/wiki/Outputs) for more information.
    
- [GAEA galaxy snapshots]({{site.baseurl}}/download/primary/gaea-hbt/gaea/)

    These are the corresponding galaxies to the HBT+ subhalos, modelled using the GAEA semi-analytical model.

- [lightcones for CSST surveys]({{site.baseurl}}/download/primary/gaea-hbt/lightcone/)

    Two lightcone catalogs are provided matching the deep and ultradeep surveys respectively.
    * [*deep field*]({{site.baseurl}}/download/primary/gaea-hbt/lightcone/deep): a 5000 deg² continuous CSST survey field with deep magnitude limits:
      - Flux limits: g<26, y<24.4, u,r,i,z, NUV<25.5
      - Field limits: R.A.: 120-210°; Dec.: 15-90°

    * [*Ultra-Deep Field*]({{site.baseurl}}/download/primary/gaea-hbt/lightcone/ultradeep): 8 deep survey fields with ultra-deep magnitude limits, each of 50 deg²:
      - Flux limits: g<27, y<25.7, u,r,i,z, NUV<26.5
      - Field centers: (230°, 50°), (180°, 50°), (130°, 40°), (150°, 10°), (30°, -20°), (50°, -40°), (345°, -30°), (330°, -60°)
      - Half opening angle: ~2.8° for each cone

Please follow the links above to browse the data files.

The redshifts of the Jiutian snapshots are provided in this [redshift list]({{site.baseurl}}/download/primary/gaea-hbt/redshift.csv).

For the snapshots, we only release one subvolume due to the substantial size of the simulation data. Each simulation is partitioned into 1000 sub-volumes based on the galaxy (or subhalo) positions at z=0, with each sub-volume representing 1/1000 of the total simulation box. Note objects may move beyond their original z=0 sub-volumes at higher redshifts. For access to the complete mock data, please contact the builders.

The released lightcone catalogs cover z=0 to z=2.5 for Jiutian-1G, and z=2.2 to z=5 for Jiutian-2G.

All released files are in HDF5 format. The main content of each file is an array of compound data (corresponding to a structure array in C) each representing a subhalo or a galaxy. Within the folder of each catalog, a markdown file contains information on the fields of the compound data type.

Each catalog contains a large number of files, each of the size of 500MB to 1GB. The sha256 checksum of all the files are also provided in a separate file for integrity verfication.

An [example shell script]({{site.baseurl}}/download/primary/gaea-hbt/JiutianDownloader.sh) is provided to download them in a loop. Simply modify the script to specify which dataset to download, and run with 

```
bash JiutianDownloader.sh
```

It will automatically download all the files of the dataset and verify its integrity.



