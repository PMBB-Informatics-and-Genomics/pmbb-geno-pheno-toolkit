# pmbb-geno-pheno-toolkit

This repository holds sub-repositories for each of the modules we have developed within the PMBB-Informatics working group.

# Our Pipelines:

## Currently Published, Cluster and Cloud-Tested:
- None yet, check back soon!

## Currently Published, Cluster-Tested:
- SAIGE FAMILY
  - ExWAS
  - GWAS
  - Gene Burden PheWAS
  - Single Variant PheWAS
- GWAS with Plink 2.0
- GWAMA for GWAS Meta-Analysis
- [PRS-CSx for Multi-Ancestry PRS Development](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-prs-csx)

## Coming Soon:
- PRS-CSx for Multi-Ancestry PRS Development

## Under Construction:
- Meta-Analysis for ExWAS Results
- LDSC Pipelines
  - Genetic Correlation
  - Heritability Estimation
  - Partitioned Heritability Estimation
- Compute PGS with Plink `--score`
- MetaXcan Pipelines

# Getting Started:
## Things to install/download:
- Nextflow (version 23+)
- Docker OR Singularity to make use of our containers
- Other pipeline-specific things you may need to build/download, such as:
  - LD Panels for PRS-CSx
  - Loki for biofilter annotations

## How to Start Working with a Pipeline:
1. Clone the sub-module for the pipeline you need
2. Edit the pipeline-specific `.config` file to include your parameters and input data
3. Set up a `nextflow.config` file with a profile for your compute system

## Resources:
- [Nextflow Hello World and Intermediate Crash Course (Google CoLab)](https://colab.research.google.com/drive/1j_2NXUYuspM79CnJngIohuzOy_X4G4qs?usp=sharing)
- Demo of Setting Up a Pipeline <- under construction

