# 🎓 Well-Calibrated and Interpretable Propensity Models for Bank Marketing


## 🔍 Overview

This repository contains the full, reproducible machine learning pipeline developed for my MSc dissertation:  
**“Well-Calibrated and Interpretable Propensity Models with Calibration and SHAP for Bank Marketing.”**

The study explores how **probability calibration** and **explainable AI (SHAP)** can improve both the reliability and interpretability of predictive models for direct marketing campaigns.  
It is based on the **UCI Bank Marketing dataset**, where the goal is to predict whether a client will subscribe to a term deposit.

---

## ✨ Key Contributions

- Developed a **fully reproducible calibration framework** comparing Logistic Regression, CatBoost, XGBoost, and a Stacking ensemble.  
- Introduced **Isotonic and Sigmoid (Platt)** calibration for improved probability reliability.  
- Evaluated models using ROC-AUC, PR-AUC, and **Brier Score** for probability calibration.  
- Integrated **SHAP interpretability** for understanding the most influential behavioral and macroeconomic factors.  
- Validated a **policy recommendation**: limiting campaign contacts to ≤3 significantly improves conversion (12.1% vs 7.5%, *p < 0.001*).

---

## 📦 Dataset

- **Source:** UCI Machine Learning Repository – Bank Marketing Data  "https://archive.ics.uci.edu/dataset/222/bank+marketing"
- **Target:** `y` (term deposit subscription: yes/no)  
- **Leakage removed:** `duration`  
- **Added features:** `was_contacted_before`, `poutcome_success`  
- **Preprocessing:** one-hot encoding, scaling, class balancing  

If you reuse this dataset, please cite the original UCI Bank Marketing paper.

---

## 🧪 Methods (Pipeline)

**1. Data Preparation**  
Cleaning, feature selection, and engineered indicators for previous contact and outcome.  
### 2️⃣ Run notebook
```bash
jupyter notebook bank_marketing_calibration.ipynb
```

---

### 3️⃣ Dataset
Place the file **`bank-additional-full.csv`** in the root folder of the repository.

---

### 4️⃣ Output
The notebook generates:
- Calibration plots  
- SHAP summary charts  
- Statistical validation (Z-test) confirming the ≤3 contact threshold  

---

## 📂 Repository Structure
```
📦 bank-marketing-calibration
│
├── data/
│   └── bank-additional-full.csv
│
├── figures/
│   └── shap_summary.png
│
├── results/
│   ├── calibration_curves.png
│   └── z_test_contacts.txt
│
├── bank_marketing_calibration.ipynb
├── final_results.html
├── Dissertation_Fereshteh_Safarkhani_2026.docx
├── requirements.txt
└── README.md
```

---

## 🔒 Ethics & Data Integrity

- Dataset is public (UCI). No personal identifiers are included.  
- All preprocessing and modeling steps are fully transparent and reproducible in the notebook.  

---
---
