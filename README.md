# 🫀 Heart Disease Detection using Machine Learning

## 📌 Project Overview
This project predicts whether a patient has **heart disease** based on clinical data such as age, cholesterol, blood pressure, and ECG results.  
We explored, cleaned, and modeled the dataset using multiple machine learning algorithms, and selected the **best performing model** for final deployment.

---

## 🎯 Objective
To develop a **reliable, interpretable, and high-performing model** that can assist in early detection of heart disease, potentially helping in preventive medical interventions.

---

## 📂 Dataset
- **Source:** Internship-provided dataset (CSV format)
- **Rows:** ~918
- **Columns:** 12 features + target
- **Target Variable:**  
  - `0` → Normal (No heart disease)  
  - `1` → Heart disease present  

**Feature Examples:**
- `age`: Patient's age in years  
- `sex`: 0 = Female, 1 = Male  
- `chest pain type`: 1–4 (various pain categories)  
- `cholesterol`: Serum cholesterol in mg/dl  
- `exercise angina`: Exercise-induced angina (0/1)  
- `st_slope`: Slope of peak exercise ST segment (1–3)  

---

## 🔍 Project Steps
1. **Data Understanding & Cleaning**
   - Checked for missing values (none found).
   - Renamed columns to consistent `snake_case`.
   - Mapped categorical codes to descriptive labels for readability.

2. **Exploratory Data Analysis (EDA)**
   - Plotted categorical and numerical features against the target.
   - Identified patterns: chest pain type, exercise angina, and ST slope were strongly related to heart disease.

3. **Data Preprocessing**
   - One-hot encoding for categorical features.
   - Standard scaling for numerical features.
   - Train/test split (80/20) with stratification.

4. **Model Training**
   - Models tested:
     - Logistic Regression
     - Random Forest
     - XGBoost
     - LightGBM

5. **Evaluation Metrics**
   - Accuracy
   - Precision, Recall, F1-Score
   - ROC AUC Score
   - Confusion Matrix Heatmaps

6. **Model Comparison**
   - LightGBM achieved **94% accuracy** and the highest ROC AUC score (0.955).
   - Balanced performance with both high precision and high recall.

---

## 🏆 Best Model: LightGBM
**Performance Highlights:**
- **Accuracy:** 94%
- **ROC AUC Score:** 0.955
- **Recall (Heart Disease):** 95% (found almost all true cases)
- **Precision (Heart Disease):** 93% (few false alarms)

**Why LightGBM Wins:**
- Excellent balance between detecting actual patients and avoiding false positives.
- Fast and efficient for structured tabular data.
- Handles categorical and numerical features well after preprocessing.

---

## 📊 Results Summary

| Model                | Accuracy | ROC AUC | Heart Disease Precision | Heart Disease Recall |
|----------------------|----------|---------|-------------------------|----------------------|
| Logistic Regression  | 0.82     | 0.896   | 0.83                    | 0.83                 |
| Random Forest        | 0.90     | 0.964   | 0.90                    | 0.91                 |
| XGBoost              | 0.92     | 0.963   | 0.92                    | 0.92                 |
| **LightGBM**         | **0.94** | **0.955** | **0.93**                | **0.95**             |

---

## 🛠 Tech Stack
- **Languages:** Python
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, lightgbm
- **Environment:** Jupyter Notebook

---

## 📄 License
This project is for educational purposes under the **MIT License**.
