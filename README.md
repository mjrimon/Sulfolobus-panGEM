# *Sulfolobus*-panGEM
## Directories
### models
This directory contains the 76 GEMs reconstructed for the *Sulfolobus*-panGEM.

**The folder GCA_000012285 contains the models from *S.acidocaldarius* reference genome (strain DSM 639).**

The folder structure looks like this:
```
models
├── genome1/
│   ├── MM_VD_1_Ni_wo_0/
│   |   ├── model1.xml
|   |   └── cured_model1/
|   |       ├── model1.xml
|   |       └── homolog_saciRefProtein/
|   |           └── **model1.xml**       
|   └── MM_aerobic_CO2_H2_glcaa/
│       ├── model1.xml
|       └── cured_model1/
|           ├── model1.xml
|           └── homolog_saciRefProtein/
|               └── **model1.xml**  
├── genome2/
|   ├── MM_VD_1_Ni_wo_0/
|   |   └── ...
|   └── sMM_aerobic_CO2_H2_glcaa/
|        └── ...

```
For every genome id (genome1) there are two GEM reconstructions depending of the medium using during the gapfilling:
* Define medium (MM_VD_1_Ni_wo_0) folder, which contains: 
  - The first reconstructed model without alterations (model 1).
  - Another folder (cured_model1), which in turn contains:
    - The cured version of the model (model1.xml).
    - Another folder (homolog_saciRefProtein), which in turn contains:
      * The cured model with the correct ids for *S.acidocaldarius* genes.
  * Complex medium (MM_aerobic_CO2_H2_glcaa/) folder, which contains the same files as the defined one.

The models inside "homolog_saciRefProtein/" folder were the ones used for the different panGEM analysis. Most of these models are the same as the cured ones, just those reconstructed from a GenBank genome (GCA) needed a change in their gene ids and because of that,these folders also contain an extra file (model1_vs_saciRefProtein.tsv) with the BLAST results. 

[![DOI](https://zenodo.org/badge/1133685978.svg)](https://doi.org/10.5281/zenodo.19254739)
