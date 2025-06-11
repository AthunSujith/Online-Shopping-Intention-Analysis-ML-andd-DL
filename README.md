# 🛒 Online Shoppers Purchasing Intention Prediction

This project focuses on analyzing and modeling a dataset to predict whether a user will generate **Revenue (True)** or not (**False**) during an online shopping session. The dataset comes from the UCI Machine Learning Repository and is ideal for classification tasks.

## 📁 Dataset Overview

- **Rows:** ~12,000
- **Target Variable:** `Revenue` (True = Buyer, False = Non-Buyer)
- **Features:** Includes data like `Administrative`, `Informational`, `ProductRelated`, `BounceRates`, `ExitRates`, `PageValues`, `Month`, `VisitorType`, etc.

---

## 📊 Goals

- Understand the key factors influencing purchasing behavior
- Handle class imbalance effectively
- Compare performance of multiple ML models
- Use metrics like accuracy, precision, recall, F1-score to evaluate

---

## 🧹 Data Preprocessing

- Handled categorical features using `LabelEncoder`
- Handled class imbalance using:
  - `class_weight='balanced'` in models
  - (Optional) SMOTE for oversampling
- Data split into training and testing sets (80/20)

---

## 🤖 Models Trained

| Model                   | Accuracy | Precision (Buyers) | Recall (Buyers) | F1-score (Buyers) |
|------------------------|----------|--------------------|-----------------|-------------------|
| Logistic Regression     | 86.1%    | 56.2%              | 75.2%           | **64.3%** ✅ Best F1 |
| Random Forest           | **89.1%**✅ | **74.9%**        | 51.6%           | 61.1%             |
| Decision Tree           | 86.0%    | 58.9%              | 53.3%           | 55.9%             |
| K-Nearest Neighbors     | 85.0%    | 61.3%              | 27.0%           | 37.5%             |
| Support Vector Machine  | 70.6%    | 33.3%              | **76.2%**       | 46.3%             |

---

## 📌 Key Findings

- Logistic Regression provided the best trade-off between precision and recall.
- Random Forest had the highest accuracy and precision.
- Class imbalance significantly affected recall for buyer prediction.
- Metrics like **F1-score** are more meaningful than accuracy in imbalanced datasets.

---

📦 online-shoppers-intention/
 ┣ 📄 online_shoppers_intention.csv
 ┣ 📄 model_analysis.ipynb
 ┣ 📄 README.md



📜 License

This project is open-source and available under the MIT License.
🤝 Contribution

Feel free to fork the repo, improve the model, try new techniques like SMOTE, XGBoost, or deep learning, and submit a PR!
