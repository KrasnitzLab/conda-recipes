# Conda recipes 

This repository contains conda recipies to build single cell computation
pipeline developed by KrasnitzLab.


## Build SCGV viewer

Example  building of SCGV viewer:

```
conda-build SCGV
```

```
conda convert conda convert --platform osx-64 ~/anaconda/envs/sgains3/conda-bld/linux-64/scgv-1.0.2-py36h39e3cac_0.tar.bz2 -o build/ 
```

```
conda upload -u krasnitzlab ~/anaconda/envs/sgains3/conda-bld/linux-64/scgv-1.0.2-py36h39e3cac_0.tar.bz2
conda upload -u krasnitzlab build/osx-64/scgv-1.0.2-py36h39e3cac_0.tar.bz2
```
