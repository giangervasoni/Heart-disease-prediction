# 🫀 Heart Failure Mortality Prediction – Interpretable Machine Learning

## 📌 Project Overview

This project presents an end-to-end, clinically grounded machine learning analysis to predict mortality in patients with heart failure. Beyond predictive performance, the primary focus is **interpretability**, **medical plausibility**, and **responsible model evaluation**.

The project is designed as a **GitHub highlight**, showcasing:

* Clean, reproducible analysis
* Clinical reasoning integrated with data science
* Model interpretability using SHAP
* Methodological awareness of bias and data leakage

---

## 🎯 Objectives

* Build a robust binary classification model to predict mortality in heart failure patients
* Compare classical statistical inference (R) with machine learning approaches (Python)
* Interpret model predictions using SHAP values
* Discuss results from a **clinical and medical perspective**
* Deliver a publication-ready notebook and professional documentation

---

## 🧬 Dataset Description

The dataset contains clinical and laboratory variables from patients diagnosed with heart failure.

### Target Variable

* **DEATH_EVENT**: Binary outcome indicating patient mortality during follow-up

### Key Predictors

* Age
* Ejection fraction
* Serum creatinine
* Serum sodium
* Platelets
* Comorbidities (diabetes, hypertension, anaemia)
* Lifestyle factors (smoking)
* Follow-up time (`time`)

> ⚠️ *Important note*: `time` represents duration of follow-up and is not a baseline clinical variable. Its inclusion is discussed critically in the interpretability section.

---

## 🛠️ Methodology

### 1️⃣ Data Preparation

* Missing value inspection and validation
* Feature scaling where appropriate
* Separation of numerical and categorical variables
* Reproducible train/test split

### 2️⃣ Modeling Strategy

* Primary model: **Tree-based classifier** (e.g., Gradient Boosting / Random Forest)
* Baseline comparison with simpler models
* Performance metrics:

  * ROC-AUC
  * Accuracy
  * Precision / Recall

### 3️⃣ Statistical Inference (R)

To demonstrate versatility and methodological rigor:

* Classical statistical analysis performed in **R**
* Logistic regression modeling
* Odds ratios and confidence intervals
* Comparison between inferential and predictive paradigms

---

## 🔍 Model Interpretability with SHAP

SHAP (SHapley Additive exPlanations) was used to understand both **global** and **local** model behavior.

### Key Findings

* Mortality risk is primarily driven by:

  * Reduced ejection fraction
  * Impaired renal function (serum creatinine)
  * Electrolyte imbalance (serum sodium)
  * Advanced age
* These variables align with established clinical prognostic factors in heart failure

### Follow-up Time Consideration

Although `time` emerged as the most influential feature:

* It reflects survival duration rather than intrinsic patient risk
* It may introduce **temporal leakage**
* Results including `time` are therefore interpreted with caution

> This explicit acknowledgment strengthens the clinical credibility of the model rather than weakening it.

---

## 🩺 Clinical Interpretation

From a medical standpoint, the model captures:

* Cardiac dysfunction severity
* Renal involvement (cardiorenal syndrome)
* Neurohormonal and electrolyte disturbances

The alignment between SHAP explanations and clinical knowledge supports the **biological plausibility** of the model outputs.

---

## ⚖️ Ethical & Methodological Considerations

* No model is intended for direct clinical decision-making
* Predictions are probabilistic, not deterministic
* Interpretability is prioritized over black-box performance
* Potential data leakage is explicitly discussed

---

## 📂 Repository Structure

```
├── heart_failure_end_to_end.ipynb      # Final, publication-ready analysis
├── README.md                # Project documentation
├── heart_failure_clinical_records_dataset.csv   # Dataset
```

---
