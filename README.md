# README: Udacity-Project_Data_Science_Blog_Post
## Installation 
## Project Motivation
Compensation in software engineering is influenced by many factors such as experience, role, industry, organization size, and geography.
However, which of these factors matter most, and how predictable compensation actually is, remains an open question.
The main motivation of this project is to answer the business question:

What are the most important features for developer compensation?

This question is answered:

using real-world survey data,
comparing two major labor markets (USA and Germany),
applying both interpretable and non-linear machine learning models,
and explaining results using SHAP (SHapley Additive Explanations).
## File Descriptions
### SO_CountryRegion_CRISPDM.ipynb
Main Python script containing the full CRISP-DM pipeline:
data loading and filtering,
data quality assessment,
cleaning and preprocessing,
exploratory data analysis,
feature selection,
model training and evaluation,
prediction scenarios,
SHAP-based explainability.
### survey_results_public_2025.csv
Raw Stack Overflow Developer Survey 2025 dataset.
### survey_results_schema.csv
Dctionary file describing all variables contained in the Stack Overflow Developer Survey 2025 dataset.  
This file provides metadata such as column names, descriptions, and intended meanings, and is used to correctly interpret survey variables during data cleaning, feature selection, and analysis.
### 2025_Developer_Survey_Tool.pdf
Official questionnaire and survey instrument for the Stack Overflow Developer Survey 2025.  
The document describes the full survey structure, question wording, answer options, and thematic sections (e.g., Learning and Career, Tech and Tech Culture, Community, AI).  
It is included for **contextual understanding only** and is **not used for feature generation or modeling**.

### bq1_pred_vs_actual/
This Folder will created by the Program SO_CountryRegion_CRISPDM.ipynb
Folder containing Predicted vs. Actual plots for Ridge and Gradient Boosting models.
### bq1_shap_plots/
This Folder will created by the Program SO_CountryRegion_CRISPDM.ipynb
Folder containing SHAP summary and feature-importance plots aggregated back to original survey features.
### README.md
Project documentation (this file).

## Summary Of The Results Of The Analysis

## Licensing, Authors, Acknowledgements
