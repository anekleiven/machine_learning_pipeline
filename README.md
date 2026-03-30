# Machine Learning Pipeline: Cancer Variant Classification 🧬🧬

This repository contains a machine learning pipeline for classifying somatic 
cancer variants from the GENIE dataset as oncogenic or likely neutral. Three 
classifiers are compared (Logistic Regression, Random Forest, XGBoost) across 
multiple feature sets, with XGBoost achieving the best performance.

The pipeline produces trained models for the three classifiers, including model evaluation
and feature importances/coefficients. 

In order to run these scripts, an annotated variant file is needed. 
Please follow the instructions in the repositories listed below. 

1. https://github.com/anekleiven/genie_oncokb_processing_scripts
2. https://github.com/anekleiven/cancer_variants_annotation_pipeline
3. https://github.com/anekleiven/explore_cancer_variants

## Requirements 💻
- Python 3.10+

## Setup Instructions 🔧

1. **Create Virtual Environment:**
`python -m venv .venv`
`. .venv/bin/activate`

2. **Install Python Requirements:**
`pip install -r requirements.txt`


## Script Descriptions 🗒️

`01_Preprocessing.ipynb`: Data preprocessing prior to exploratory analysis (create new columns, feature selection for modeling, create ML-dataframe, filter variants to target oncogenic classes, check for missing values, handle missing gnomAD_AF values). 

`02_Exploratory_Analysis.ipynb`: Exploratory data analysis prior to ML (initial data inspection, descriptive statistics, missing value analysis, target value analysis, gene distribution analysis, univariate analysis, multivariate analysis, top genes). 

`03_Data_preparation.ipynb`: Data processing prior to ML-modeling (log transformation, map target to binary numbers, remove gene names, feature engineering, data splitting, identify outliers, save datasets). 

`04_Model_Training.ipynb`: ML-modeling and model evaluation (Logistic regression, Random Forest and XGBoost. Hyperparameter tuning, model fitting and evaluation). 


## Recommended Sources 🛜

- AACR Project GENIE: https://www.aacr.org/professionals/research/aacr-project-genie/
- OncoKB: https://www.oncokb.org


