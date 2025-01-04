# pmbb-geno-pheno-toolkit

This repository has an overview of our sub-repositories for each of the modules we have developed within the PMBB-Informatics working group. Contents include:
- Links to repos
- Example config files
- Set-up instructions

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

# Getting Started:
## Things to install/download:
- Nextflow (version 23 is ideal)
- Docker OR Singularity to make use of our containers
- Other pipeline-specific things you may need to build/download, such as:
  - LD Panels for PRS-CSx
  - Loki for biofilter annotations

## How to Start Working with a Pipeline:
1. Clone the sub-module for the pipeline you need
2. Edit the pipeline-specific `.config` file to include your parameters and input data
3. Set up a `nextflow.config` file with a profile for your compute system. We have an example for this as well [HERE](https://github.com/PMBB-Informatics-and-Genomics/pmbb-geno-pheno-toolkit/Example_Configs/nextflow.config). 
4. Pro Tip: at the top of your `nextflow.config`, add a line: `includeConfig {pipeline}.config` with the relative path to your new `.config` file. The alternative is using the `-c` / `-config` flag when calling the pipeline.
5. In order to run one of the workflows, you will use a command like this: `nextflow run /path/to/pmbb-nf-toolkit-{pipeline}/{pipeline}.nf`. More details can be found in module-specific READMEs

## Resources:
- [PMBB Website](https://pmbb.med.upenn.edu/)
- [All of Us Home](https://allofus.nih.gov/)
- [nf-core Getting Started guide](https://nf-co.re/docs/usage/getting_started/introduction)
- [Nextflow-provided training](https://training.nextflow.io/hello_nextflow/)
- [Nextflow Hello World and Intermediate Crash Course (Google CoLab)](https://colab.research.google.com/drive/1j_2NXUYuspM79CnJngIohuzOy_X4G4qs?usp=sharing)
- [Nextflow Hello Penguins: Real Data Exaple](https://colab.research.google.com/drive/1yjGTaMOFiCmr99-bnsAJ01XcLA7xkWdB)



