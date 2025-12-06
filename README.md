# 🧠 Clinical Decision Support System (CDSS) for Early Identification of Obesity-Related Complication Risk

**Course:** SAT 5141 – Clinical Decision Support and AI Modeling  
** Contributors - *Frederick Damptey & Benjamin Odoom Asomaning*

---

This repository contains the development pipeline, codebase, and documentation for a **machine learning–driven Clinical Decision Support System (CDSS)** aimed at predicting **obesity-related complication risk**.

The project integrates **AutoGluon Tabular**, **explainable AI tools**, and a **Streamlit clinician-in-the-loop interface** interactive tool to support clinical screening and preventive care.

---

## 📌 Project Overview

Obesity remains one of the most significant public health challenges worldwide, contributing to rising rates of **Type 2 diabetes, hypertension, and cardiovascular disease**. Early identification of individuals at high risk allows for timely intervention and improved outcomes.

This CDSS performs **multi-class classification** to predict patients’ obesity categories using demographic, lifestyle, and anthropometric data - offering clinicians an **interpretable, transparent, and data-driven decision-support tool**.

## 🏥 Clinical Problem

Obesity-related complications cover a broad spectrum of **metabolic and cardiovascular disorders**. Clinicians increasingly require tools that:

- ✅ Identify individuals at high or increasing risk  
- ✅ Provide interpretable insights into health, lifestyle, and dietary contributors  
- ✅ Enable early screening and support in resource-limited settings  

This project fulfills those needs using an AI-assisted risk estimation model built from **behavioral, demographic, and biological** factors.

---

## 🧬 Dataset Description

**Source:** [Obesity Risk Dataset (Kaggle, 2024)](https://www.kaggle.com/)  
**Size:** Over 20,000 samples × 17 features  

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
•	Data cleaning 

---

## ⚙️ Methodology

### 🔁 Machine Learning Pipeline

1. **Data Ingestion**  
2. **Preprocessing:** Cleaning, train_test_split, reconversion of test_train-split to df
3. **Model Training (AutoGluon Tabular):** Derivatives of the models below
   - Random Forest  
   - XGBoost
   - LightGBM  
   - CatBoost  
   - Neural Network  
   - Ensemble optimization using balanced accuracy  
4. **Evaluation Metrics:** Accuracy, Sensitivity, Specificity, F1-score, ROC-AUC  
5. **Explainable AI:**
   - SHAP (implemented)  

6. **Clinician-in-the-Loop Prototype:**  
   Streamlit-based interface for clinical output, feedback and transparency, allowing decision validation, override and logging.

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

 
These results demonstrate **strong predictive validity** and **robust generalization** across methods.

---

## 🧩 Explainability

SHAP analysis highlights the top contributing predictors:
- Weight, height and gender
- Frequency of physical activity  
- Nutritional and lifestyle behaviors  

---

## 🖥 Further “Clinician-in-the-Loop” App Development

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
- Explainable AI for outcome transparency  
- No personally identifiable information (PII) used  

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

👉 Video Link: https://youtu.be/lHVb6tY_ybI?si=tTPhcDG36oRSLzIf 

---

## 🤝 Team Contributions

| Team Member | Roles |
|--------------|--------|
| **Frederick Damptey** | Model design from data ingestion to audit Clinician-in-the-loop. |
| **Benjamin Odoom Asomaning** | Theoretical foundation, dataset acquisition and literature review, model evaluation and report writing.

---

## ⚠️ Project Disclaimer

This project is for **educational and research purposes only.**  
It is **not a certified diagnostic tool** and must **not** be used for patient care without regulatory approval.  
Model outputs are designed to **support**, not replace, professional medical judgment.

