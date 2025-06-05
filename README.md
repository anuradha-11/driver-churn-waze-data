# 🚗 Waze Driver Churn Prediction

This project analyzes user engagement and churn behavior in the Waze navigation app. The goal was to identify behavioral and device-related patterns associated with user retention, and to build machine learning models to predict driver churn using classification techniques.

---

## 📊 Key Findings

- **Retention Rate**: 82% of users were retained, while 18% churned — creating a moderately imbalanced dataset.
- **Missing Labels**: Of the 700 rows with missing churn labels, 64% were iPhone users and 36% Android users.
- **Device Type vs. Engagement**:
  - iPhone users showed slightly higher average drives than Android users.
  - Hypothesis testing showed **no statistically significant difference** (p > 0.05) in drive behavior by device type.
- **Professional Drivers Churn Less**:
  - Churn rate among **professional drivers** was 7.6%, compared to 19.9% for non-professionals.
- **Model Weakness**:
  - All models struggled with recall, especially in identifying actual churners.
  - Models produced **3x more false negatives than false positives**, meaning they often missed true churn cases.

---

## 🤖 Model Evaluation Summary

| Model            | Precision | Recall | F1 Score | Accuracy |
|------------------|-----------|--------|----------|----------|
| RF (CV)          | 0.457     | 0.125  | 0.197    | 81.87%   |
| XGB (CV)         | 0.425     | 0.179  | 0.252    | 81.12%   |
| RF (Validation)  | 0.453     | 0.124  | 0.195    | 81.82%   |
| XGB (Validation) | 0.396     | 0.176  | 0.243    | 80.63%   |
| XGB (Test)       | 0.416     | 0.201  | 0.271    | 80.84%   |

🔎 Despite decent accuracy, the models had **low recall**, indicating poor performance at detecting churned users — a crucial metric for real-world retention efforts.

---

## 🛠️ Tools & Libraries Used

- Python, Jupyter Notebook
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`, `xgboost`
- Classification Models: `RandomForestClassifier`, `XGBClassifier`
- Evaluation Metrics: Precision, Recall, F1 Score, Accuracy, Confusion Matrix

---

## 📁 Files in this Repo

- `waze_proj.ipynb` – Main analysis and modeling notebook
- `waze_dataset.csv` – Input data (if included or linked separately)

---

## 📬 Contact

**Anuradha Ramasagaram**  
📧 anuradha.r2098@gmail.com  
🎓 MS Business Analytics, University of North Texas

---
