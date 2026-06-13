# Breast Cancer Survival Prediction using Clinical and Genomic Data

## Overview

This project builds interpretable machine learning models to predict breast cancer survival using the METABRIC dataset (1904 patients), combining both clinical variables and gene expression data.

The main goal is to explore whether adding genomic biomarkers to standard clinical features improves predictive performance, while keeping the model interpretable enough for clinical use.

Rather than focusing only on accuracy, the emphasis is on **explainability and clinical relevance**.

---

## Dataset

**Source:** METABRIC (Molecular Taxonomy of Breast Cancer International Consortium)  
**Patients:** 1904  

### Clinical Features
- Age at diagnosis  
- Tumor size  
- Histological grade  
- ER / HER2 status  
- Hormone therapy status  
- Lymph node involvement  
- Nottingham Prognostic Index  

### Genomic Features
- Gene expression profiles  
- Top 20 prognostic genes selected using statistical testing  
- Genes associated with survival differences across patient groups  

---

## Methodology

### 1. Data Exploration
- Clinical feature distributions and survival patterns
- Survival outcome imbalance analysis
- Gene expression profiling

### 2. Genomic Analysis
- Differential gene expression between survival groups
- Statistical significance testing (t-tests)
- Identification of survival-associated biomarkers

### 3. Machine Learning Models
Models trained using different feature sets:
- Clinical features only  
- Genomic features only  
- Combined clinical + genomic features  

Models used:
- Logistic Regression  
- Random Forest  
- Gradient Boosting  

---

## Results

| Model | Clinical ROC-AUC | Genomic ROC-AUC | Combined ROC-AUC |
|------|------------------|-----------------|------------------|
| Logistic Regression | 0.693 | 0.667 | **0.734** |
| Random Forest | 0.679 | 0.663 | 0.733 |
| Gradient Boosting | 0.698 | 0.649 | 0.724 |

The best performance was achieved using a **Logistic Regression model trained on combined clinical + genomic features (ROC-AUC ≈ 0.734)**.

---

## Model Interpretability

To ensure clinical usability and transparency, the following explainability methods were applied:

- Feature importance analysis  
- SHAP-based explanations  
- Patient-level risk stratification  
- Calibration analysis  
- Prediction reliability assessment  

---

## Key Insights

- Combining clinical and genomic data improved predictive performance compared to using either alone  
- Genes such as **GSK3B, JAK1, CASP8, KMT2C, and TGFBR2** showed strong associations with survival outcomes  
- SHAP analysis helped identify how specific clinical and genetic factors influence individual predictions

---

## Visualizations

### Model Performance Comparison
![Model Comparison](figures/model_comparison.png)

### SHAP Explainability (Feature Importance)
![SHAP Summary](figures/shap_summary.png)

### Patient Risk Stratification
![Risk Stratification](figures/risk_stratification.png)

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- SHAP  

---

## Future Work

- Validation on external independent datasets  
- More robust cross-validation strategies  
- Integration of additional omics data  
- Extension toward clinical decision-support systems  

---

## Note

This project focuses on **interpretable machine learning for biomedical applications**, not just predictive modeling accuracy.
