# Breast Cancer Survival Prediction using Clinical and Genomic Data

## Overview

This project develops interpretable machine learning models for predicting breast cancer survival using clinical and genomic data from the METABRIC cohort.

The objective is to investigate whether integrating gene-expression biomarkers with clinical variables can improve survival prediction while maintaining clinical interpretability.

---

## Dataset

- Source: METABRIC (Molecular Taxonomy of Breast Cancer International Consortium)
- Total Patients: 1904
- Clinical Variables:
  - Age at diagnosis
  - Tumor size
  - Histological grade
  - ER status
  - HER2 status
  - Hormone therapy status
  - Lymph node involvement
  - Nottingham Prognostic Index

- Genomic Variables:
  - Differentially expressed genes associated with survival outcomes
  - Top 20 prognostic genes selected through statistical analysis

---

## Methodology

### Exploratory Data Analysis
- Clinical feature exploration
- Survival outcome analysis
- Gene expression distribution analysis

### Gene Expression Analysis
- Differential expression analysis between survival groups
- Independent t-tests
- Identification of survival-associated biomarkers

### Machine Learning Models
- Logistic Regression
- Random Forest
- Gradient Boosting

Models were evaluated on:

- Clinical Features Only
- Genomic Features Only
- Combined Clinical + Genomic Features

---

## Results

| Model | Clinical ROC-AUC | Genomic ROC-AUC | Combined ROC-AUC |
|---------|---------|---------|---------|
| Logistic Regression | 0.693 | 0.667 | 0.734 |
| Random Forest | 0.679 | 0.663 | 0.733 |
| Gradient Boosting | 0.698 | 0.649 | 0.724 |

The integrated clinical-genomic Logistic Regression model achieved the best overall performance.

---

## Model Interpretability

To improve transparency and clinical relevance:

- Feature importance analysis
- SHAP explainability
- Risk stratification
- Calibration analysis
- Patient-level prediction assessment

were performed.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- SHAP

---

## Key Findings

- Integration of clinical and genomic data improved predictive performance.
- Several genes including GSK3B, JAK1, CASP8, KMT2C, and TGFBR2 showed significant associations with survival outcomes.
- Explainable AI methods provided biologically interpretable insights into model predictions.

---

## Future Work

- External validation on independent cohorts
- Cross-validation-based model assessment
- Integration of additional omics data
- Development of clinical decision-support tools
