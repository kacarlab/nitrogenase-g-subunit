# G subunit 

## Summary

The G subunit is one of the few cases of innovation in the nitrogenase
enzyme. Our research applies computational methods to dive into its origins
and functions. This repository contains the code required to reproduce
some of our analysis.

## Important note: nomenclature

In these notebooks we use the original codes to refer to each of the ancestors:

- Anc263 : Ancestor of Vnf and Anf
- Anc264 : Ancestor previous to Vnf and Anf (Anc-Nif in the article text)
- Anc262 : Ancestor of Vnf
- Anc330 : Ancestor of Anf
- Anc265 : Ancestor previous to Anc264


## Installation

We recommend the usage of conda environments to ease the installation
of all code dependencies. Miniconda can be downloaded from its [webpage]().
To install the environment, just run:

    conda create --file environment.yml

There are some packages that we could not install through conda. Paste the
following comments here:

    pip install pyfamsa
    pip install logomaker

We carry out some of our analysis in Jupyter Notebooks, inside the 
**notebooks** folder.

## Prediction of structures

We employed the colabfold_batch implementation of colabfold in our HPC cluster (CHTC). 
The code for that implementation is available at its github repo. We called the
program as:

    colabfold_batch --amber --templates --num-recycle 3 --use-gpu-relax dkghh.colabready.csv dkghh.results

Where dkghh.colabready.csv is a file located in the seq folder.


## Contents

- **data**:
    - *foldseek/*
    - *prs/*
    - *signatures/*
    - *surface-network/*
    - ala-scan.AC.csv
    - foldseek.matches.csv
- **figures**: 
- **models**: structures predicted through ColabFold
- **notebooks**: 
- **seq**:
- **structure**: structures obtained from PDB

## Contact

For any issue, mail: cuevaszuviri at wisc.edu
