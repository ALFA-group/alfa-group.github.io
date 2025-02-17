---
layout: page 
title: Resources
permalink: /resources
---

## Computational analysis of single-cell RNA-seq data

In collaboration with many others, we develop and maintain this [teaching resource](https:www.singlecellcourse.org) for teaching scRNAseq analysis.

## Computational tools

All of our computational tools are available at our [GitHub](https://github.com/hemberg-lab) site. Please note that some of the older tools may not be actively supported any more as the people responsible for coding have moved on.

### Spatial transcriptomics methods

* [SCOTIA](https://github.com/Caochris/SCOTIA) is a python package for discovery of ligand-receptor interactions from high-resolution spatial transcriptomics data.

* [SpatialQuery](https://github.com/ShaokunAn/Spatial-Query) is a python package for identifying cell type patterns in high resolution spatial transcriptomics data. 

### Single-cell methods

* [SC3](https://www.bioconductor.org/packages/release/bioc/html/SC3.html) is an R package for unsupervised clustering of scRNAseq data based on transcriptional profile.

* [scmap](https://www.bioconductor.org/packages/release/bioc/html/scmap.html) is an R package for mapping cells onto a reference dataset.

* [souporcell](https://github.com/wheaton5/souporcell) is a method for clustering cells by genotype rather than transcriptional profile. Note that souporcell does not require a reference genotype as it will automatically detect variants from your reads.

* [M3Drop](http://www.bioconductor.org/packages/release/bioc/html/M3Drop.html) is an R package for feature selection for scRNAseq analysis.

* [SC3s](https://github.com/hemberg-lab/sc3s/) is a python package for unsupervised clustering based on transcription profiles. It is highly recommended to use this package instead of the original SC3.

* [scover](https://github.com/jacobhepkema/scover) is a neural network model in python for *de novo* discovery of regulatory motifs from single-cell data.

* [scfind](https://github.com/hemberg-lab/scfind) is an R package for fast searches of single-cell data.

* [scHumanNet](https://github.com/netbiolab/scHumanNet) is an R package for reference guided construction of gene networks in human.

### Other genomics methods

* [MicroExonator](https://github.com/hemberg-lab/MicroExonator) is a [snakemake](https://snakemake.readthedocs.io/en/stable/) pipeline for *de novo* discovery and quantification of short exons.

* [TransposonUltimate](https://github.com/DerKevinRiehl/TransposonUltimate) is a bundle of tools in python for analyzing transposable elements.

* [MPRAnator](https://www.sanger.ac.uk/tool/mpranator/) is a webtool for design of massively parallel reporter assays.


