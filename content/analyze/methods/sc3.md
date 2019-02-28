---
path: "/analyze/methods/methods-packages/sc3"
date: "2018-09-14"
title: "Single-cell consensus clustering (SC3)"
author: "Martin Hemberg (SC3), EBI team (sc3-scripts)"
description: "SC3 is an unsupervised clustering method for scRNA-seq data."
githubUrl: "https://github.com/hemberg-lab/SC3"
appUrl: "http://bioconductor.org/packages/SC3"
upstreamRegistryUrl: "http://bioconductor.org/packages/SC3"
componentName: "analysisDetail"
---

[![Build Status](http://www.bioconductor.org/shields/build/release/bioc/SC3.svg)](https://git.bioconductor.org/packages/SC3)

[SC3](http://bioconductor.org/packages/SC3) is an unsupervised clustering method for scRNA-seq data. SC3 also estimates the number of clusters and it provides features to aid the biological interpretation of the clusters. [sc3-scripts](https://anaconda.org/bioconda/sc3-scripts) provides a set of simple wrappers with robust argument parsing for individual components of the SC3 package.

# Use

```
docker pull quay.io/repository/biocontainers/sc3-scripts:<version>
```

How to perform unsupervised clustering on scRNA-seq data (already QCed and normalised) in a SingleCellExperiment object 

```
curl -L -o deng-reads.rds https://github.com/hemberg-lab/scRNA.seq.course/raw/master/deng/deng-reads.rds

docker run -v ${PWD}:/data -w /data --rm quay.io/repository/biocontainers/sc3-scripts:<version> sc3-sc3.R -i deng-reads.rds -o deng-sc3.rds 
```

# Validate 
Run this command to confirm your container produces correct reference output:

```
docker run -v ${PWD}:/data -w /data --rm quay.io/repository/biocontainers/sc3-scripts:<version> sc3-sc3-validate.R
```

# Contact
Martin Hemberg, SC3 (<a href="mailto://mh26@sanger.ac.uk">mh26@sanger.ac.uk</a>)
EBI team, sc3-scripts (<a href="mailto://team@ebi.ac.uk">team@ebi.ac.uk</a>)