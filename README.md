# Conda recipes 

This repository contains conda recipies to build single cell computation
pipeline developed by KrasnitzLab.


## Build SCGV viewer

Example  building of SCGV viewer:

```bash
conda-build SCGV
```

To convert linux package into OSX-64 package use:

```bash
conda convert --platform osx-64 ~/anaconda/envs/sgains3/conda-bld/linux-64/scgv-1.0.2-py36h39e3cac_0.tar.bz2 -o build/ 
```

To upload conda packages into Anaconda Cloud channel for KrasnitzLab use:

```bash
anaconda upload -u krasnitzlab ~/anaconda/envs/sgains3/conda-bld/linux-64/scgv-1.0.2-py36h39e3cac_0.tar.bz2
anaconda upload -u krasnitzlab build/osx-64/scgv-1.0.2-py36h39e3cac_0.tar.bz2
```

To install `SCGV` use:

```bash
conda install -c krasnitzlab scgv
```


## Build SCclust package


We need to build with `bioconda` channel because of
`bioconductor-dnacopy` dependency:



```
conda build -c bioconda SCclust
```


To convert linux package into OSX-64 package use:
```
conda convert --platform osx-64 ~/anaconda/envs/sgains3/conda-bld/linux-64/scclust-1.0.0RC3-r341_1.tar.bz2 -o build/ 
```

To upload conda packages into Anaconda Cloud channel for KrasnitzLab use:

```
anaconda upload -u krasnitzlab ~/anaconda/envs/sgains3/conda-bld/linux-64/scclust-1.0.0RC3-r341_1.tar.bz2
anaconda upload -u krasnitzlab build/osx-64/scclust-1.0.0RC3-r341_1.tar.bz2
```

To install `SCclust` package use:

```
conda install -c krasnitzlab scclust
```

