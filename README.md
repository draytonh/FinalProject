# FinalProject

### Description
This project looks at differential gene expression in Caucasian females vs. African American females with endometrial cancer. African American women have been found to have double the mortality rate of Caucasian females, so it is conceivable that they would have varied gene expression enriched in their tumors. 
This will be written-up in a R Notebook that can be run as a vignette. 

## Table of Contents
1) Dataset Installation
2) Proposal
a) Proposed Analysis
b) Proposed Timeline and Major Milestones
c) User interface
3) Required packages
4) Usage
5) Web Interface
6) Known Issues

## 1) Dataset Installation 
Samples were selected from the NIH National Cancer Institute GDC Data Portal and were filtered for White and Black or African American race, not Hispanic or Latino ethnicity. The files were filtered to be from the TCGA-UCEC project, the disease type to be cystic, mucinous, or serous neoplasms (as these are clinically more severe malignancies), the experimental strategy as RNA-Seq, and the workflow type as HTSeq-Counts.
To download files, apply the filteres described above (or utilize the below url), go to each individual file name on the TCGA website, and select download. 

Samples: Black or African American n = 25, Caucasian n = 50

https://portal.gdc.cancer.gov/repository?facetTab=cases&filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.demographic.ethnicity%22%2C%22value%22%3A%5B%22not%20hispanic%20or%20latino%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.demographic.race%22%2C%22value%22%3A%5B%22black%20or%20african%20american%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.disease_type%22%2C%22value%22%3A%5B%22Cystic%2C%20Mucinous%20and%20Serous%20Neoplasms%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.project.project_id%22%2C%22value%22%3A%5B%22TCGA-UCEC%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.analysis.workflow_type%22%2C%22value%22%3A%5B%22HTSeq%20-%20Counts%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.experimental_strategy%22%2C%22value%22%3A%5B%22RNA-Seq%22%5D%7D%7D%5D%7D&searchTableTab=files

## 2) Proposal
### a) Proposed Analysis
RNA-seq analysis will be conducted in R studios using the limma, Glimma, and egdeR libraries. 

### b) Proposed Timeline and Major Milestones
Week 1 - Get RNA-seq vignette to work with unit test as outlined in "RNA-seq analysis is easy as 1-2-3 with limma, Glimma and edgeR" (Law et al. 2018)
https://www.bioconductor.org/packages/devel/workflows/vignettes/RNAseq123/inst/doc/limmaWorkflow.html

Week 2 - Create dataframes for selected samples

Week 3 - Run RNA-seq analysis on dataframes

### c) User Interface
This analysis will be presented in a R Notebook and will be workable as a vignette for which other similar differential gene expression analyses using RNA-seq data may be performed.

## 3) Required Packages
limma, Glimma, edgeR, Homo.sapiens, gplots

## 4) Usage
Generate an R Notebook in RStudio utilizing the executable script in the endometrialrnaseq file.

## 5) Web Interface
R-Publication: http://rpubs.com/draytonh/finalendometrialrnaseq

## 6) Known Issues
1) When creating the control matrix, only a column for those above the age of 70 (LT70) is generated, not for those above the age of 70 (GT70). This may be due to a sorting issue and may require for the samples to be entered in a different order.
2) The camera method was unable to be used for either the original vignette this project was based on or utilizing the sample data for this project. This may be an issue within the original script of the original vignette. 


