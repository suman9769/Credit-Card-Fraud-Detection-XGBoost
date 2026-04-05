# 💳 Advanced Credit Card Fraud Detection Pipeline
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange)
![Imbalanced-Learn](https://img.shields.io/badge/Technique-SMOTE-green)
![Status](https://img.shields.io/badge/Status-Complete-success)
## 📌 Project Overview
Credit card fraud costs businesses billions of dollars annually. The primary challenge in building a detection model is the **extreme class imbalance** (e.g., 99.8% normal transactions vs. 0.2% fraudulent). This project builds a production-ready, leak-proof Machine Learning pipeline designed to maximize **Recall** and securely catch fraudulent behavior without bleeding synthetic data into the validation set.
## 🚀 Technical Highlights
- **Algorithm:** eXtreme Gradient Boosting (`XGBoost`)
- **Handling Imbalance:** Applied **SMOTE** (Synthetic Minority Over-sampling Technique) strictly inside an `imblearn Pipeline` to prevent data leakage during cross-validation.
- **Hyperparameter Tuning:** Automated `GridSearchCV` optimization prioritizing **Recall** over Accuracy.
- **Data Scaling:** Implemented `StandardScaler` to handle drastic variance in transaction Amount distributions.
## 📊 Key Results
By optimizing the model specifically for Recall in an imbalanced geometric space, the pipeline achieved:
* **Recall:** ~88% (Successfully catching nearly 90% of all fraudulent hackers).
* **Accuracy:** 98.8%
*(Note: Precision was intentionally sacrificed as a business tradeoff. In banking, the financial cost of a False Negative far outweighs the customer-service cost of a False Positive).*
## 📈 Visualizations
This project includes extensive Exploratory Data Analysis (EDA) and Model Evaluation metrics, featuring:
1. **Targeted Correlation Analysis:** Highlighting the specific PCA components (like `V17`, `V14`) that heavily dictate fraud probability.
2. **Amount Density Estimation (KDE):** Visually proving the disparity in spending behavior between safe customers and thieves.
3. **Color-Coded Confusion Matrix:** Translating raw prediction arrays into immediately actionable business insights.
## 🛠 Libraries Used
* `pandas`, `numpy`, `matplotlib`, `seaborn`
* `scikit-learn` (`GridSearchCV`, `StandardScaler`, `Metrics`)
* `xgboost` (`XGBClassifier`)
* `imbalanced-learn` (`SMOTE`, `Pipeline`)
