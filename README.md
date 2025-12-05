# 🧠 Clinical Decision Support System (CDSS) for Early Identification of Obesity-Related Complication Risk

**Course:** SAT 5141 – Clinical Decision Support and AI Modeling  
**Team:** Group 5 — *Frederick Damptey & Benjamin Odoom Asomaning*

---

This repository contains the development pipeline, codebase, and documentation for a **machine learning–driven Clinical Decision Support System (CDSS)** aimed at predicting **obesity-related complication risk**.

The project integrates **AutoGluon Tabular**, **explainable AI tools**, and a planned **Streamlit clinician-in-the-loop interface** to support clinical screening and preventive care.

---

## 📌 Project Overview

Obesity remains one of the most significant public health challenges worldwide, contributing to rising rates of **Type 2 diabetes, hypertension, and cardiovascular disease**. Early identification of individuals at high risk allows for timely intervention and improved outcomes.

This CDSS performs **multi-class classification** to predict patients’ obesity categories using demographic, lifestyle, and anthropometric data — offering clinicians an **interpretable, transparent, and data-driven decision-support tool**.


## 🏥 Clinical Problem

Obesity-related complications cover a broad spectrum of **metabolic and cardiovascular disorders**. Clinicians increasingly require tools that:

- ✅ Identify individuals at high or increasing risk  
- ✅ Provide interpretable insights into health, lifestyle, and dietary contributors  
- ✅ Enable early screening and support in resource-limited settings  

This project fulfills those needs using an AI-assisted risk estimation model built from **behavioral, physiological, and environmental** factors.

---

## 🧬 Dataset Description

**Source:** [Obesity Risk Dataset (Kaggle, 2024)](https://www.kaggle.com/)  
**Size:** 20,000 samples × 17 features  

**Target Labels (7 BMI-based classes):**
- Insufficient Weight  
- Normal Weight  
- Overweight Level I  
- Overweight Level II  
- Obesity Type I  
- Obesity Type II  
- Obesity Type III  

**Key Variables:**
- Age and gender  
- Dietary habits and caloric intake  
- Physical activity patterns  
- Family health history  
- Height and weight (engineered into BMI)

**Data Validation Steps:**
- Z-score outlier detection  
- Stratified k-fold evaluation  
- Normalization and encoding  
- Full de-identification verification  

---

## ⚙️ Methodology

### 🔁 Machine Learning Pipeline

1. **Data Ingestion**  
2. **Preprocessing:** Normalization, scaling, and encoding categorical variables  
3. **Feature Engineering:** Derived BMI, caloric balance, and activity indices  
4. **Model Training (AutoGluon Tabular):**
   - Random Forest  
   - LightGBM  
   - CatBoost  
   - Neural Network  
   - Ensemble optimization using balanced accuracy  
5. **Evaluation Metrics:** Accuracy, Sensitivity, Specificity, F1-score, ROC-AUC  
6. **Explainable AI:**
   - SHAP (implemented)  
   - LIME (planned)  
7. **Clinician-in-the-Loop Prototype:**  
   Streamlit-based interface for decision validation, override, and logging

---

## 🛠 Notebook Execution

The Jupyter notebook automates key tasks such as:
- Model comparison and leaderboard generation  
- Ensemble selection optimization  
- Metric computation and visualization  
- SHAP-based feature importance plotting  

---

## 📊 Preliminary Results

**Performance Summary (based on Progress Report):**

| Model | Train Accuracy | Validation Accuracy | Balanced Accuracy | ROC-AUC |
|--------|----------------|---------------------|-------------------|----------|
| XGBoost | 0.997 | 0.95 | 0.90 | 0.99 |
| CatBoost | 0.997 | 0.90 | 0.90 | 0.98 |
| Random Forest | 1.00 | 0.90 | 0.89 | 0.98 |

These results demonstrate **strong predictive validity** and **robust generalization** across methods.

---

## 🧩 Explainability

SHAP analysis highlights the top contributing predictors:
- BMI  
- Caloric intake  
- Frequency of physical activity  
- Nutritional and lifestyle behaviors  

Explainability ensures that clinicians understand model outputs and retain final judgment authority in care decisions.

---

## 🖥 Clinician-in-the-Loop App *(Upcoming)*

The future **Streamlit interface** will allow clinicians to:

- Upload patient profiles  
- View model predictions and SHAP explanations  
- Approve, reject, or override system recommendations  
- Record reasoning for audit purposes  

This configuration mitigates **automation bias** and ensures **clinical accountability**.

---

## 🔐 Ethics, Security, and Legal Considerations

- Fully de-identified dataset  
- HIPAA-aligned system design  
- Fairness and bias monitoring integrated into evaluation steps  
- Explainable AI for outcome transparency  
- No personally identifiable information (PII) used  

Refer to *Section 5* of the project report for full ethical and legal discussion.

---

## 🚧 Future Work

- Hyperparameter optimization  
- Model calibration  
- Integration of multi-source datasets  
- Enhanced explainability (LIME integration)  
- Streamlit application deployment  
- Pilot testing with simulated patient data  

---

## 🎥 Recorded Presentation Video

A narrated walkthrough of the project and CDSS prototype is available below:

👉 Video Link: Add your YouTube, Google Drive, or GitHub video link here


---

## 🤝 Team Contributions

| Team Member | Roles |
|--------------|--------|
| **Frederick Damptey** | Model design from data ingestion to audit Clinician-in-the-loop. |
| **Benjamin Odoom Asomaning** | Data Ingestion and preprocessing, literature review, model evaluation and report writing. |

---

## ⚠️ Project Disclaimer

This project is for **educational and research purposes only.**  
It is **not a certified diagnostic tool** and must **not** be used for patient care without regulatory approval.  
Model outputs are designed to **support**, not replace, professional medical judgment.

---
