# pmbb-geno-pheno-toolkit

This repository holds sub-repositories for each of the modules we have developed within the PMBB-Informatics working group.

# Our Pipelines:

## Currently Published + Cluster and AOU-Tested:
- [GWAS with PLINK 2.0](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-plink-2.0-gwas)
- [GWAMA for GWAS Meta-Analysis](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-gwama-meta-analysis)
- [Meta-Analysis for ExWAS Results](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-exwas-meta-analysis)

## Currently Published + Cluster-Tested:
- [SAIGE FAMILY](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family)
  - ExWAS
  - GWAS
  - Gene Burden PheWAS
  - Single Variant PheWAS
- [PRS-CSx for Multi-Ancestry PRS Development](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-prs-csx)

## Coming Soon:
- Compute PGS with Plink `--score`
- PLINK Clump
- MetaXcan Pipelines

## Under Construction:
- LDSC Pipelines
  - Genetic Correlation
  - Heritability Estimation
  - Partitioned Heritability Estimation
- OMOP-based simple phenotyping

## How to Start Working with a Pipeline:
1. Clone the sub-module for the pipeline you need
2. Edit the pipeline-specific `.config` file to include your parameters and input data
3. Set up a `nextflow.config` file with a profile for your compute system

## Resources:
- [Nextflow Hello World and Intermediate Crash Course (Google CoLab)](https://colab.research.google.com/drive/1j_2NXUYuspM79CnJngIohuzOy_X4G4qs?usp=sharing)
- [Nextflow Hello Penguins: Real Data Exaple](https://colab.research.google.com/drive/1yjGTaMOFiCmr99-bnsAJ01XcLA7xkWdB)
- Demo of Setting Up a Pipeline <- under construction

