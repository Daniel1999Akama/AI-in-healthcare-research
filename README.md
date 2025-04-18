# 🧠 Pneumonia Prediction Using Machine Learning

This project applies machine learning to structured clinical data to predict pneumonia in patients. By leveraging dimensionality reduction and ensemble modeling, the goal is to create an interpretable and performant tool that supports early diagnosis, particularly in resource-limited settings.

---

## 📌 Project Overview

Pneumonia is a major cause of mortality worldwide. Traditional diagnosis methods often rely on imaging, which is not always accessible. This project investigates how structured clinical data (e.g., age, symptoms, lab results) can be used to build a predictive model for pneumonia risk.

---

## 🧪 Methodology

### 1. **Data Preprocessing**
- Removed columns with high missing values
- Imputed missing data (median for numeric, mode for categorical)
- Standardized numeric features
- Encoded categorical variables using Label Encoding

### 2. **Dimensionality Reduction**
- Applied **Principal Component Analysis (PCA)** to reduce 70+ features
- Retained 95% of data variance with significantly fewer components

### 3. **Class Imbalance Handling**
- Used **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the dataset

### 4. **Model Training**
- Trained and evaluated the following models:
  - Logistic Regression
  - Random Forest Classifier
  - XGBoost Classifier

---

## 📊 Model Performance

| Model               | Accuracy | Precision (Weighted Avg) | Recall (Weighted Avg) | F1-Score (Weighted Avg) |
|---------------------|----------|---------------------------|------------------------|--------------------------|
| Logistic Regression | 0.933    | 0.96                      | 0.93                   | 0.95                     |
| Random Forest       | 0.966    | 0.96                      | 0.97                   | 0.96                     |
| XGBoost             | 0.980    | 0.96                      | 0.98                   | 0.97                     |

> 📝 *Note: While accuracy is high, performance on minority classes remains low — a common challenge in healthcare datasets.*

---

## 🧬 Explainability

- Used **PCA Loadings** to identify the most influential original features per principal component
- Key features included: `age`, `admission_psi`, `etio_pneumo_patogen`, `comorbid`, and `weight`
- Visualizations include:
  - Top PCA component loadings
  - ROC curves for model comparison

---

## 📈 Visualizations

- PCA variance explained plot
- Top feature loadings per PC (bar chart)
- ROC curves comparing models
- Confusion matrices (optional)

---

## 🔮 Future Work

- Combine structured data with image-based inputs (e.g., chest X-rays)
- Apply deep learning techniques like transfer learning
- Explore federated learning for privacy-preserving, diverse datasets
- Deploy as a web app for real-world clinical use

---

## Reproducibility
Download the zip folder that contains the dataset and the IPYNB FILE


