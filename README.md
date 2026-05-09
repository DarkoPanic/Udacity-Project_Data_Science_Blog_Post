# README: Udacity-Project_Data_Science_Blog_Post
## Installation 
This project is implemented in **Python** and relies exclusively on **scikit-learn (version 1.6.1)** and standard data science libraries.
### Requirements
- Python ≥ 3.10  
- scikit-learn == 1.6.1  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- shap (for explainability)

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
Automatically generated output folder containing Predicted vs. Actual plots for Ridge and Gradient Boosting models.
### bq1_shap_plots/
Automatically generated output folder containing SHAP summary and feature-importance plots aggregated to original survey features.
### README.md
Project documentation (this file).

## Summary Of The Results Of The Analysis
### Model Performance
Compensation is only moderately predictable using survey features alone.
Best performance (after robust trimming of extreme values):
USA: R² ≈ 0.28
Germany: R² ≈ 0.37
Non-linear models consistently outperform linear baselines, but the improvement is modest.

### Ridge vs. Histogram Gradient Boosting
Ridge Regression provides a strong, stable linear baseline and handles high-dimensional one-hot encoded features well.
Histogram Gradient Boosting Regressor (HGBR) captures non-linear effects and feature interactions (e.g., experience saturation, role × industry interactions).
HGBR achieves slightly better R² and RMSE in both countries.

### Key Drivers (SHAP Analysis)
Across both countries, work experience is the most influential factor.
Additional important drivers differ by country:

USA: Industry, developer role, organization size
Germany: Organization size, structured role definitions, education-related features

SHAP analysis shows that compensation is driven by combinations of features, not single variables in isolation.

### Interpretation
Survey features explain part of compensation differences, but a large share remains unexplained.
Factors such as company-specific pay bands, negotiation, equity, bonuses, and fine-grained location effects are not captured in the dataset.

## Licensing, Authors, Acknowledgements
### License
This project is released under the MIT License.
### Author
Darko Panic, Dr.-Ing.
### Acknowledgements
Stack Overflow for making the Developer Survey 2025 publicly available.
The open-source Python and scikit-learn communities.
SHAP for providing state-of-the-art model explainability tools.
The survey structure and variable context are based on the official Stack Overflow Developer Survey 2025 questionnaire/tool.
