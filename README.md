# ✈ Aircraft Risk Prediction using Machine Learning & Explainable AI

## 📌 Overview
This project presents a complete machine learning pipeline for predicting aircraft operational risk using engine sensor data.

The system integrates:
- ✅ Data Validation using Great Expectations  
- ✅ Exploratory Data Analysis (EDA)  
- ✅ Random Forest Classification  
- ✅ SHAP-based Explainability  
- ✅ Fairness & Bias Evaluation  

The objective is to build a model that is not only accurate but also transparent and reliable for safety-critical environments.

---

## 🧠 Problem Statement
Aircraft engines operate under extreme mechanical and thermal stress.  
Traditional threshold-based monitoring systems may fail to capture complex nonlinear interactions between sensor parameters.

This project uses machine learning to intelligently detect risky operating conditions.

---

## 📊 Features Used

| Feature | Description |
|----------|------------|
| vibration_rms | Root Mean Square vibration amplitude |
| rpm | Rotations per minute of engine shaft |
| temperature | Engine temperature (°C) |
| acoustic_db | Noise intensity in decibels |

### 🎯 Target Variable
- 0 = Safe  
- 1 = Risk  

---

## ⚙ System Architecture

Sensor Data  
→ Data Validation  
→ EDA  
→ Model Training  
→ Model Evaluation  
→ SHAP Explainability  
→ Fairness Analysis  

---

## 🤖 Model Used
**Random Forest Classifier**

Why Random Forest?
- Handles nonlinear relationships  
- Robust to noise  
- Reduces overfitting via ensemble learning  
- Provides feature importance  

---

## 📈 Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  

Special focus: minimizing **False Negatives**, as missed risk detection is critical in aviation systems.

---

## 🔬 Explainability (SHAP)

SHAP analysis revealed feature importance ranking:

vibration_rms > temperature > acoustic_db > rpm  

High vibration levels significantly increase predicted risk probability.

---

## ⚖ Fairness Analysis
Model performance was evaluated across RPM groups:
- Low RPM  
- Medium RPM  
- High RPM  

No significant bias was observed across operational groups.

---

## 🛠 Tech Stack
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- SHAP  
- Great Expectations  
- Matplotlib  
- Jupyter Notebook  

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook