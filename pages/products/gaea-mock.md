---
title: Jiutian GAEA Mock Catalog
permalink: /gaea-mock/
layout: work
---

## Overview

The mock catalogs presented here are introduced in the [GAEA mock paper](coming-soon..). 

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

## Data Access
We release four types of catalogs, including the GAEA galaxy snapshots, the HBT+ subhalo snapshots, and lightcones for CSST deep and ultradeep surveys.

For the snapshots, we only release one subvolume due to the substantial size of the simulation data. Each simulation is partitioned into 1000 sub-volumes based on the galaxy (or subhalo) positions at z=0, with each sub-volume representing 1/1000 of the total simulation box. Note objects may move beyond their original z=0 sub-volumes at higher redshifts. For access to the complete mock data, please [contact the builders](#contact) below.

The released lightcone catalogs cover z=0 to z=2.5 for Jiutian-1G, and z=2.2 to z=5 for Jiutian-2G.

All released files are in HDF5 format.

- ### [Snapshot - Redshift Table]({{site.baseurl}}/download/CSSTmock/redshift.csv) for Jiutian Simulations

- ### GAEA Galaxy Snapshots
  [Field Description]({{site.baseurl}}/download/CSSTmock/SAM/SAM.md)

  | Simulation               | File List | Download Script |
  |--------------------------|-----------|-----------------|
  | **Jiutian-1G Subvolume001** | [Files]({{site.baseurl}}/download/CSSTmock/SAM/M1G/) | [Script]({{site.baseurl}}/download/CSSTmock/SAM/M1G/download_M1G_SAM.sh) |
  | **Jiutian-2G Subvolume002** | [Files]({{site.baseurl}}/download/CSSTmock/SAM/M2G/) | [Script]({{site.baseurl}}/download/CSSTmock/SAM/M2G/download_M2G_SAM.sh) |

- ### HBT+ Subhalo Snapshots
  [Field Description]({{site.baseurl}}/download/CSSTmock/HBT/HBT.md)

  | Simulation               | File List | Download Script |
  |--------------------------|-----------|-----------------|
  | **Jiutian-1G Subvolume001** | [Files]({{site.baseurl}}/download/CSSTmock/HBT/M1G/) | [Script]({{site.baseurl}}/download/CSSTmock/HBT/M1G/download_M1G_HBT.sh) |
  | **Jiutian-2G Subvolume002** | [Files]({{site.baseurl}}/download/CSSTmock/HBT/M2G/) | [Script]({{site.baseurl}}/download/CSSTmock/HBT/M2G/download_M2G_HBT.sh) |

- ### CSST Deep Field
  **5000 deg² continuous CSST survey field** with deep magnitude limits:
  - Flux limits: g<26, y<24.4, u,r,i,z, NUV<25.5
  - Field limits: R.A.: 120-210°; Dec.: 15-90°
    
  [Field Description]({{site.baseurl}}/download/CSSTmock/lightcone/lightcone.md)

  | Simulation     | File List | Download Script |
  |----------------|-----------|-----------------|
  | **Jiutian-1G** | [Files]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M1G/) | [Script]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M1G/download_M1G_Deep.sh) |
  | **Jiutian-2G** | [Files]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M2G/) | [Script]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M2G/download_M2G_Deep.sh) |

- ### CSST Ultra-Deep Field
  **8 × 50 deg² cone CSST survey fields** with ultra-deep magnitude limits:
  - Flux limits: g<27, y<25.7, u,r,i,z, NUV<26.5
  - Field centers: (230°, 50°), (180°, 50°), (130°, 40°), (150°, 10°), (30°, -20°), (50°, -40°), (345°, -30°), (330°, -60°)
  - Half opening angle: ~2.8° for each cone
 
   [Field Description]({{site.baseurl}}/download/CSSTmock/lightcone/lightcone.md)

  | Simulation     | File List | Download Script |
  |----------------|-----------|-----------------|
  | **Jiutian-1G** | [Files]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M1G/) | [Script]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M1G/download_M1G_Ultradeep.sh) |
  | **Jiutian-2G** | [Files]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M2G/) | [Script]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M2G/download_M2G_Ultradeep.sh) |

<a id="contact"></a>   
## Contact Information

- [Zhenlin Tan](mailto:zltan999@sjtu.edu.cn) (Shanghai Jiao Tong University)
- [Jiaxin Han](mailto:jiaxin.han@sjtu.edu.cn) (Shanghai Jiao Tong University)
