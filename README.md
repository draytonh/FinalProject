# FinalProject

## Description
This project looks at differential gene expression in Caucasian females vs. African American females with endometrial cancer. Black women have been found to have double the mortality rate of Caucasian females, so it is conceivable that they would have varied gene expression enriched in their tumors. 
This will be written-up in a R Notebook that can be run as a vignette. 

## Datasets
Samples were selected from the NIH National Cancer Institute GDC Data Portal and were filtered for White and Black or African American race, not Hispanic or Latino ethnicity. The files were filtered to be from the TCGA-UCEC project, the disease type to be cystic, mucinous, or serous neoplasms (as these are clinically more severe malignancies), the experimental strategy as RNA-Seq, and the workflow type as HTSeq-Counts.

Samples: Black or African American n = 25, Caucasian n = 50

https://portal.gdc.cancer.gov/repository?facetTab=cases&filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.demographic.ethnicity%22%2C%22value%22%3A%5B%22not%20hispanic%20or%20latino%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.demographic.race%22%2C%22value%22%3A%5B%22black%20or%20african%20american%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.disease_type%22%2C%22value%22%3A%5B%22Cystic%2C%20Mucinous%20and%20Serous%20Neoplasms%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.project.project_id%22%2C%22value%22%3A%5B%22TCGA-UCEC%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.analysis.workflow_type%22%2C%22value%22%3A%5B%22HTSeq%20-%20Counts%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.experimental_strategy%22%2C%22value%22%3A%5B%22RNA-Seq%22%5D%7D%7D%5D%7D&searchTableTab=files

## Proposed Analysis
RNA-seq analysis will be conducted in R studios using the limma, Glimma, and egdeR libraries. 

## Proposed Timeline and Major Milestones
Week 1 - Get RNA-seq vignette to work with unit test as outlined in "RNA-seq analysis is easy as 1-2-3 with limma, Glimma and edgeR" (Law et al. 2018)
https://www.bioconductor.org/packages/devel/workflows/vignettes/RNAseq123/inst/doc/limmaWorkflow.html

Week 2 - Create dataframes for selected samples

Week 3 - Run RNA-seq analysis on dataframes

## User Interface
This analysis will be presented in a R Notebook and will be workable as a vignette for which other similar differential gene expression analyses using RNA-seq data may be performed.
