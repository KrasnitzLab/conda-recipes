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

We need to build using `krasnitzlab` channel because of
`bioconductor-dnacopy` dependency:

```bash
conda build -c krasnitzlab SCclust
```

To convert linux package into OSX-64 package use:

```bash
conda convert --platform osx-64 ~/anaconda/envs/sgains3/conda-bld/linux-64/scclust-1.0.0RC3-r341_1.tar.bz2 -o build/ 
```

To upload conda packages into Anaconda Cloud channel for KrasnitzLab use:

```bash
anaconda upload -u krasnitzlab ~/anaconda/envs/sgains3/conda-bld/linux-64/scclust-1.0.0RC3-r341_1.tar.bz2
anaconda upload -u krasnitzlab build/osx-64/scclust-1.0.0RC3-r341_1.tar.bz2
```

To install `SCclust` package use:

```bash
conda install -c krasnitzlab scclust
```

## Build sGAINS pipeline

Example  building of sGAINS:

```bash
# conda build sgains
conda build -c bioconda -c krasnitzlab sgains
```

To upload conda package into Anaconda Cloud channel for KrasnitzLab use:

```bash
anaconda upload -u krasnitzlab /home/lubo/anaconda3/conda-bld/linux-64/sgains-1.0.0-py36h39e3cac_1.tar.bz2
```

To install use:

```bash
conda install -c bioconda -c krasnitzlab sgains
```