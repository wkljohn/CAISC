# CAISC
CAISC, which stands for Clonal Architecture with Integrating SNV and CNV, is a software that integrates copy number variation and single nucleotide mutations for genetic heterogeneity profiling and subclone detection by single-cell RNA sequencing 
## Questions?
If you have any questions about using CAISC, you can open a new issue [here](https://github.com/lizamathews/CAISC/issues/new), or you can email one of the maintainers listed below. 
## Installation
Install to R/RStudio and install all packages in the latest version of R.
```R
devtools::install_github("lizamathews/CAISC")
```
## Pipeline
We present Clonal Architecture with Integration of SNV and CNV (CAISC), a new subclone detection algorithm that integrates both SNV and CNV data in order to acquire more accurate and robust clustering results. Here is an overview of the CAISC pipeline. We derive two cell-cell distance matrices using either SNV and CNV data, from DENDRO and infercnv respectively. These matrices are integrated using an entropy weighted method, and into a final distance matrix that is used to cluster the cells into subclones.

<p align="center">
  <img src='https://raw.githubusercontent.com/lizamathews/CAISC/master/figure1.jpg'>
</p>

**Figure 1.** Clonal Architecture with Integration of SNV and CNV (CAISC). Overview of the computational framework that integrates both SNV and CNV profiles for clonal identification from scRNA-seq data. scRNA-seq reads are aligned with STAR, mutations are identified with GATK, and the read counts were calculated to represent gene expression. DENDRO is used to calculate a distance matrix based on allele reads of mutations. Infercnv is used to convert gene expression level data to a CNV profile matrix and then to calculate a distance matrix between cells. These two distance matrices are integrated using an entropy weighted method. Finally, a clonal tree is generated using the integrated matrix to more accurately identify subclones and infer their evolutionary relationship. The interactive figure generated by interactiveComplexHeatmap allows for manual examination of inferred clones.

## Vignette
## Citation
CAISC: A Software to Integrate Copy Number Variation and Single Nucleotide Mutations for Genetic Heterogeneity Profiling and Subclone Detection by Single-cell RNA Sequencing ([GitHub](https://github.com/lizamathews/CAISC))
## Developers and Maintainers
* Shouguo Gao (shouguo.gao@nih.gov)
* Jeerthi Kannan (jeerthi98@gmail.com)
* Liza Mathews (lizamathews5@gmail.com)
