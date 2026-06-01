# Cytotoxicity Classification Model for PHBV Polymers

This repository contains all the files used for developing a classification model to predict the cytotoxicity of PHBV-based polymers using machine learning techniques in the ANIPH project.

## Table of Contents

- [Data](#data)
  - [cytotoxicity_data.csv](#cytotoxicity_datacsv)
  - [cytotoxicity_database.xlsx](#cytotoxicity_databasexlsx)
  - [final_train_set_cytotoxicity.xlsx](#final_train_set_cytotoxicityxlsx)
  - [final_test_set_cytotoxicity.xlsx](#final_test_set_cytotoxicityxlsx)
  - [sample_20_cytotoxicity.xlsx](#sample_20_cytotoxicityxlsx)
  - [mi_scores_cytotoxicity.xlsx](#mi_scores_cytotoxicityxlsx)
- [Notebooks](#notebooks)
  - [cytotoxicity_data_preprocess.ipynb](#cytotoxicity_data_preprocessipynb)
  - [cytotoxicity_rf_classifier_no outliers.ipynb](#cytotoxicity_rf_classifier_no-outliersipynb)
  - [cytotoxicity_rf_classifier_outliers.ipynb](#cytotoxicity_rf_classifier_outliersipynb)
- [Plots](#plots)

## Data

This folder contains all data files used in the study.

#### cytotoxicity_data.csv
The full curated cytotoxicity dataset including all features and metadata used for model development.

#### cytotoxicity_database.xlsx
The raw cytotoxicity database compiled from literature, containing polymer composition descriptors and toxicity labels.

#### final_train_set_cytotoxicity.xlsx
The final training set (80% of the dataset) after stratified splitting, used for model training and cross-validation.

#### final_test_set_cytotoxicity.xlsx
The final test set (20% of the dataset) used for independent model evaluation.

#### sample_20_cytotoxicity.xlsx
A 20-row sample of the training set for inspection and reporting purposes.

#### mi_scores_cytotoxicity.xlsx
Mutual information scores for each feature relative to the target variable, used for feature selection analysis.

## Notebooks

#### cytotoxicity_data_preprocess.ipynb
Exploratory data analysis and unit conversion for the raw cytotoxicity dataset.

#### cytotoxicity_rf_classifier_no outliers.ipynb
Main classification pipeline using the Extra Trees Classifier without outlier removal. Includes model selection, Optuna hyperparameter tuning, applicability domain assessment, and SHAP explainability analysis.

#### cytotoxicity_rf_classifier_outliers.ipynb
Alternative classification pipeline with outlier removal applied during preprocessing, used for comparison with the main pipeline.

## Plots

Contains all figures generated during the analysis:
- Kendall correlation heatmap of numerical features
- Confusion matrices for training and test sets
- SHAP bar plot and beeswarm plot for model interpretability

## Author

Alexandros Angelis — NTUA, School of Chemical Engineers