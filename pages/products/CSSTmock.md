---
title: Jiutian GAEA Mock Catalog
permalink: /CSSTmock/
layout: work
---

## Overview

The CSST mock catalogs presented here are introduced in Paper: [Jiutian mock light-cone](https://arxiv.org/abs/2503.21368). We utilize Jiutian-1G to construct light-cones from z=0 to z=2.5, and Jiutian-2G for light-cones from z=2.2 to z=5.

## Simulation Specifications

| Simulation    | Boxsize (Mpc/h) | Softening (kpc/h) | Particle Mass (M⊙/h) | Particles | Snapshots | Cosmology |
|---------------|-----------------|-------------------|----------------------|-----------|-----------|-----------|
| Jiutian-1G    | 1000            | 4.0               | 3.723 × 10^8         | 6144^3    | 128       | Planck 2018 (Ω_m=0.3111, h=0.6766) |
| Jiutian-2G    | 2000            | 7.0               | 2.978 × 10^9         | 6144^3    | 128       | Planck 2018 (Ω_m=0.3111, h=0.6766) |

## GAEA Model Parameters

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

For additional SAM parameters, refer to [Xie et al. 2020](https://arxiv.org/abs/2003.12757).

## Data Structure

Due to the substantial size of the simulation data, we process and release it in subdivided volumes. Each simulation is partitioned into 1000 sub-volumes based on galaxy positions at z=0, with each sub-volume representing 1/1000 of the total simulation box. This corresponds to sub-volume sizes of 100 Mpc/h for Jiutian-1G and 200 Mpc/h for Jiutian-2G.

While particle motion occurs globally and objects may move beyond their original z=0 sub-volumes at higher redshifts, we maintain the 1/1000 volume representation for statistical consistency across redshifts.

## Data Release

Our first release includes:

1. **GAEA snapshot outputs** of a subvolume
2. **HBT+ snapshot outputs** of the same subvolume
3. **5000 deg² continuous CSST survey field** with deep magnitude limits:
   - Flux limits: g<26, y<24.4, u,r,i,z, NUV<25.5
   - Field limits: R.A.: 120-210°; Dec.: 15-90°
4. **8 × 50 deg² cone CSST survey fields** with ultra-deep magnitude limits:
   - Flux limits: g<27, y<25.7, u,r,i,z, NUV<26.5
   - Field centers: (230°, 50°), (180°, 50°), (130°, 40°), (150°, 10°), (30°, -20°), (50°, -40°), (345°, -30°), (330°, -60°)
   - Half observation angle: ~2.8° for each cone

All released files are in HDF5 format.

## Catalog Access

### [Snapshot - Redshift Table]({{site.baseurl}}/download/CSSTmock/redshift.csv) for Jiutian Simulations

### GAEA SAM Snapshot Outputs
[Field Description]({{site.baseurl}}/download/CSSTmock/SAM/SAM.md)

- **Jiutian-1G Subvolume001**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/SAM/M1G/download_M1G_SAM.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/SAM/M1G/)

- **Jiutian-2G Subvolume002**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/SAM/M2G/download_M2G_SAM.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/SAM/M2G/)

### HBT Subhalo Snapshot Outputs
[Field Description]({{site.baseurl}}/download/CSSTmock/HBT/HBT.md)

- **Jiutian-1G Subvolume001**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/HBT/M1G/download_M1G_HBT.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/HBT/M1G/)

- **Jiutian-2G Subvolume002**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/HBT/M2G/download_M2G_HBT.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/HBT/M2G/)

### CSST Deep Field (5000 deg² Survey)
[Field Description]({{site.baseurl}}/download/CSSTmock/lightcone/lightcone.md)

- **Jiutian-1G**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M1G/download_M1G_Deep.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M1G/)

- **Jiutian-2G**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/lightcone/Deep/M2G/download_M2G_Deep.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/Deep/M2G/)

### CSST Ultra-Deep Field (8 × 50 deg² Survey)

- **Jiutian-1G**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M1G/download_M1G_Ultradeep.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M1G/)

- **Jiutian-2G**
  - [Auto-download Script]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M2G/download_M2G_Ultradeep.sh)
  - [File List]({{site.baseurl}}/download/CSSTmock/lightcone/Ultradeep/M2G/)

## Contact Information

- [Zhenlin Tan](mailto:zltan999@sjtu.edu.cn) (Shanghai Jiao Tong University)
- [Jiaxin Han](mailto:jiaxin.han@sjtu.edu.cn) (Shanghai Jiao Tong University)
