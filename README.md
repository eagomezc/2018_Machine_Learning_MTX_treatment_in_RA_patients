# Machine Learning models to predict response to DMARD treatment in rheumatoid arthritis patients using lipid mediator profiles

# Overview: 

This repository contains the **R scripts** used to create the machine learning models used to predict the response to DMARD treatment in rheumatoid arthiritis patients using lipid mediators profiles, clinical scores, specific lipid mediator families and separating the data based on the pathotype showed by the patients. 

Besides that, it also contains the scripts used for the validation step of the models (using a validation cohort) and the Matthews correlation coefficient (MCC) calculation. 

Finally, it also contains a small script that was used to do the **differential gene expression analysis** of the ALOX12, ALOX5, ALOX15 and ALOX15B enzymes. 

**NOTE:** **MetaboAnalyst web-based application** (more information [here](https://www.metaboanalyst.ca//faces/ModuleView.xhtml)) (version 4.0) was used to perform some statistical analyses such as partial least squares-discrimination analysis (PLS-DA), orthagonal partial least squares-discrimination analysis (oPLS-DA), variance importance in projection analysis (VIP). For the network analyses, [**Cytoscape software**](https://cytoscape.org/) (version 3.7.1) was used.

# System Requierements: 

## Hardware requierements: 

All the scripts and software used in the paper *Blood pro-resolving mediator profiles are linked with synovial pathology and predict DMARD responsiveness in rheumatoid arthritis* were run in a standar computer (RAM: 8GB, CP$: 4 cores, 3.60 GHZ/core) with a maximum runtime of aprox. 10 minutes for the more demanding script ([**1_classyfire_(SVM_models).R**](https://github.com/eagomezc/2019_Machine_Learning_DMARD_in_RA_patients/blob/master/b_R_Scripts/1_classyfire_(SVM_models).R)). 

A computer with lower specs (e.g. 2GB of RAM) will work but some scripts will take longer to run. 

## System requierements:

All the R scripts were created and used on **Windows 10**:

**R version**: 3.5.1 
**R Studio version**: 1.1.456

The script should be compatible with Mac and Linux operating systems. 

For installing R and R Studio, follows the installation instructions [here](https://www.stats.bris.ac.uk/R/) and [here](https://www.rstudio.com/products/rstudio/download/). 

## Requiered R packages (libraries): 

The requiered packages to run all the scripts contained in this repository can be installed as follow: 

The last version of classyfire (0.1-2) package can be found [here](https://cran.r-project.org/src/contrib/Archive/classyfire/)

```
# Packages classyfire:
# After download the last version of classyfire (0.1-2), you can install the package as follow, specifying the directory of the zip: 
install.packages("C:pathToDirectory/classyfire_0.1-2.tar.gz", 
                  repos = NULL, 
                  type = "source")
                  
# Packages ggplot2, randomForest and mltools:
install.packages(c('ggplot2', 'randomForest', 'mltools'))

# Package edgeR from Bioconductor:
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("edgeR")
```
# Content: 

The repository contains three folders: 

## [a_Toy_Data](https://github.com/eagomezc/2019_Machine_Learning_DMARD_in_RA_patients/tree/master/a_Toy_Data)

This repository contains, separated by subfolders, the different file formats (as toy data) that has to be used to run the different R scripts. Each subfolder has the name of the specific script where they can be used, in addition to the number of script, to make more clear what file is used in what folder. At the moment to download this repository in a local computer, it's important to remember that all the **pathways in the scripts has to be changed**.






