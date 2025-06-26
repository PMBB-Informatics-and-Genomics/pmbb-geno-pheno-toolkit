# pmbb-geno-pheno-toolkit

This repository serves as a landing page of our repositories for each of the modules we have developed within the PMBB-Informatics working group. Contents include:
- Links to repos
- Example config files
- Set-up instructions

# Our Pipelines:

| Pipeline | Description | Local Cluster | AOU-tested | DNAnexus-tested | In-development |
|----------|-------------|---------------|------------|-----------------|----------------|
| [GWAS with PLINK 2.0](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-plink-2.0-gwas) | Genome-wide association studies using PLINK 2.0 | ✅ | ✅ | ❌ | ❌ |
| [SAIGE Family of Pipelines](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family/tree/main) | SAIGE Family of Association Studies | ✅ | ✅ | ✅ | ✅ |
| ├─[SAIGE ExWAS](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family/blob/main/READMEs/SAIGE_ExWAS_docs.md) | Exome-wide association studies using SAIGE | ✅ | ❌ | ❌ | ❌ |
| ├─[SAIGE GWAS](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family/blob/main/READMEs/SAIGE_GWAS_docs.md) | Genome-wide association studies using SAIGE | ✅ | ❌ | ❌ | ❌ |
| ├─[SAIGE GATE](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family/blob/5bcf1ea047af318269c7204f35b1dd17b8b087a7/READMEs/SAIGE-GATE_docs.md) | Genetic Analysis of Time-to-Event phenotypes | ✅ | ❌ | ❌ | ❌ |
| ├─[SAIGE Gene Burden PheWAS](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family/blob/main/READMEs/Single-Gene_Burden_PheWAS_docs.md) | Phenome-wide association studies using gene burden testing | ✅ | ❌ | ❌ | ❌ |
| └─[SAIGE Single Variant PheWAS](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-saige-family/blob/main/READMEs/Single-Variant_PheWAS_docs.md) | Phenome-wide association studies for single variants | ✅ | ❌ | ❌ | ❌ |
| [GWAS Meta-Analysis with GWAMA](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-gwama-meta-analysis) | Meta-analysis of GWAS results using GWAMA | ✅ | ✅ | ❌ | ❌ |
| [ExWAS Meta-Analysis](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-exwas-meta-analysis) | Meta-analysis pipeline for ExWAS results | ✅ | ✅ | ❌ | ❌ |
| [PRS-CSx for Multi-Ancestry PRS Development](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-prs-csx) | Multi-ancestry polygenic risk score development | ✅ | ❌ | ❌ | ❌ |
| [Compute PGS with Plink 2.0 Score](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-plink2-score) | Computing polygenic scores using Plink score Function | ✅ | ❌ | ❌ | ❌ |
| [PLINK Clump](https://github.com/PMBB-Informatics-and-Genomics/pmbb-nf-toolkit-prs-csx) | Finding variants that belong to a GWAS signal via LD-based variant clumping | ✅ | ✅ | ❌ | ❌ |
| MetaXcan Pipelines | Gene-based association testing pipelines | ❌ | ❌ | ❌ | ✅ |
| LDSC Genetic Correlation | Genetic correlation analysis using LDSC | ❌ | ❌ | ❌ | ✅ |
| LDSC Heritability Estimation | SNP-based heritability estimation | ❌ | ❌ | ❌ | ✅ |
| LDSC Partitioned Heritability Estimation | Partitioned heritability analysis | ❌ | ❌ | ❌ | ✅ |
| OMOP-based simple phenotyping | Simple phenotyping based on OMOP data model | ❌ | ❌ | ❌ | ✅ |


# Getting Started

## Setup - Install/download:
- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- A text editor for updating the `nextflow.config` profile and the pipeline-specific `.config` file such as `vim` or `nano`
- [Nextflow version 23.04.1.5866](https://www.nextflow.io/docs/latest/cli.html)
- [Singularity version 3.8.3](https://sylabs.io/docs/) OR [Docker version 4.30.0](https://docs.docker.com/)
- [JDK version 11.0.5](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html)
- Other pipeline-specific things you may need to build/download, such as:
  - LD Panels for PRS-CSx
  - Loki for biofilter annotations

## Overview of Steps to get started with one of our pipelines:
1. Clone the desired pipeline's (a.k.a. module) git repo. 
2. Set up a `nextflow.config` file with a profile for your compute system. An example for this can be found here: [Nextflow Config](https://github.com/PMBB-Informatics-and-Genomics/pmbb-geno-pheno-toolkit/Example_Configs/nextflow.config).
  - After this `nextflow.config` file is set up once, it can be used for all of our pipelines. We recommend creating it once and symlinking it for each tool. 
  - Note: Nextflow will ALWAYS look for (and expect) a `nextflow.config` in your running directory. 
3. Create a pipeline-specific `.config` file specifying your parameters and input files. Examples can be found in our Pipeline-Specific [Example Config Files](https://github.com/PMBB-Informatics-and-Genomics/pmbb-geno-pheno-toolkit/Example_Configs/).
4. Run the workflow using a command like this: `nextflow run /path/to/pmbb-nf-toolkit-{pipeline}/{pipeline}.nf`. More details can be found in module-specific READMEs

## Resources:
- [PMBB Website](https://pmbb.med.upenn.edu/)
- [All of Us Home](https://allofus.nih.gov/)
- [Nextflow Hello World and Intermediate Crash Course (Google CoLab)](https://colab.research.google.com/drive/1j_2NXUYuspM79CnJngIohuzOy_X4G4qs?usp=sharing)
- [nf-core Getting Started guide](https://nf-co.re/docs/usage/getting_started/introduction)
- [Nextflow-provided training](https://training.nextflow.io/hello_nextflow/)
