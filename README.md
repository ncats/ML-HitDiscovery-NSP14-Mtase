# Discovery of SARS-CoV-2 NSP14-Mtase Inhibitors by Harnessing Scaffold-Centric Exploration of the Enamine Ultra-Large Chemical Space
This repository is under the NCATS organization. It documents computational workflows, datasets, and results from the drug discovery campaign focused on discovering potential inhibitors for the SARS-CoV-2-NSP14-Mtase protein. This study employs machine learning (ML) models trained on high-throughput screening data, followed by the scaffold-centric exploration against the Enamine REAL space, to identify promising hit compounds. 

**Project Overview**
The primary goal of this research work is to identify and validate compounds with potential inhibitory activity against the SARS-CoV-2 NSP14-Mtase protein, an essential viral protein involved in viral replication. This work was conducted as part of the Antiviral Program for Pandemics (APP) project at the National Center for Advancing Translational Sciences (NCATS). 

**Key Objectives**  
- Development of two machine learning models using quantitative high throughput screening (qHTS) experimental assay data to predict activity against the NSP14-Mtase
- Perform virtual screening using optimized ML models to identify promising hit compounds from the in-house Genesis  and Sytravon molecular library.
- Perform the similarity-based screening of the hit compounds for hit expansion.
- Hit-to-lead optimization via scaffold-centric exploration of the Ultra-Large Enamine Library.

**Repository Contents**  
This repository contains the following:

**Screening Data**

- **_Dataset Files:_**
- `Dataset file for 1st model/`: This folder contains dataset compounds from different screened libraries in .xlsx format, used for the first model preparation.
- `Dataset file for 2nd model/`: This folder contains dataset compounds from different screened libraries in .xlsx format, used for the second model preparation.
  
- `all dataset molecules for 1st model.sdf`: All the dataset molecules in .sdf format, used for the first model preparation.
- `all dataset molecules for the second model.sdf`: All the dataset molecules in .sdf format, were used for the second model preparation.

**KNIME Workflows**
- _Hyperparameter Optimization Workflows_:

- **_For the 1st Model:_**
  - `Hyperparameter optimization for Gradient Boost model for 1st round of modeling.knwf`: A workflow for hyperparameter optimization of Gradient Boost model, using different combinations of Avalon, Morgan, and FeatMorgan fingerprints along with RDKit descriptors for the first round of modelling.

  - `Hyperparameter optimization for XGBoost model for 1st round of modeling.knwf`: A workflow for hyperparameter optimization of the XGBoost model, using different combinations of Avalon, Morgan, and FeatMorgan fingerprints along with RDKit descriptors for the first round of modelling.

  - `Hyperparameter optimization for Random Forest model for 1st round of modeling.knwf`: A workflow for hyperparameter optimization of the Random Forest model, using different combinations of Avalon, Morgan, and FeatMorgan fingerprints along with RDKit descriptors for the first round of modelling.
 
- **_For the 2nd Model:_**
  - `Hyperparameter optimization for Gradient Boost model for 2nd round of modeling.knwf`: A workflow for hyperparameter optimization of the Gradient Boost model, using different combinations of Avalon, Morgan, and FeatMorgan fingerprints along with RDKit descriptors for the second round of modelling.

  - `Hyperparameter optimization for XGBoost model for 2nd round of modeling.knwf`: A workflow for hyperparameter optimization of the XGBoost model, using different combinations of Avalon, Morgan, and FeatMorgan fingerprints along with RDKit descriptors for the second round of modelling.

  - `Hyperparameter optimization for Random Forest model for 2nd round of modeling.knwf`: A workflow for hyperparameter optimization of the Random Forest model, using different combinations of Avalon, Morgan, and FeatMorgan fingerprints along with RDKit descriptors for the second round of modelling.
 
- _Virtual Screening Workflow_:    
  - `NSP14 1st round of screening against Genesis library.knwf`: Represents the virtual screening workflow against the Genesis molecular library, using the best, optimized ML model for hit discovery as a first round of screening.
  - `NSP14 2nd round modeling + Sytravon screening + Enamine screening.knwf`: Represents the virtual screening workflow against the Sytravon molecular library, using the best, optimized ML model for hit discovery as a second round of screening and Enamine library screening for scaffold-centric exploration.

- _Analog Screening_:
   - `Analog compound search.knwf`: Workflow for identifying analog compounds around the hit compounds obtained from the first and second rounds of screening.

 **Prediction and Results Files**

 - `1st set Prediction based on classification model.xlsx`: An excel file listing the top predicted hit compounds identified from the first round of virtual screening against Genesis library.

- `2nd set Prediction based on classification model.xlsx`: An excel file listing the top predicted hit compounds identified from the second round of virtual screening against Sytravon library.

- `2D PCA for 1st set model.csv`: All dataset compounds with PCA values for scatter plot visualization.

- `Selected 78 Enamine compounds for order.xlsx`: List of 78 compounds selected for ordering from Enamine.

  **_Substructure Search Results:_**

   - `Substructure-search results on left hand side modification.xlsx`: Results of scaffold-centric left-hand side exploration of hit molecules.

   - `Substructure-search results on right hand side modification.xlsx`: Results of scaffold-centric right-hand side exploration of hit molecules.
