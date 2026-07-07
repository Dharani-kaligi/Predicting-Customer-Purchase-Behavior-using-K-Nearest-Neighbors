# Social Network Ads Purchase Prediction using KNN

## 📌 Project Overview

This project focuses on predicting whether a customer will purchase a product after viewing a social media advertisement using the **K-Nearest Neighbors (KNN)** classification algorithm.

The objective is to build a machine learning model that helps businesses identify potential customers based on their demographic information and improve targeted marketing strategies.

---

## 🎯 Business Problem

Companies invest heavily in digital advertising. Identifying customers who are more likely to purchase helps optimize marketing campaigns and improve customer targeting.

This project predicts customer purchase behavior using:

- **Age**
- **Estimated Salary**

Target Variable:

- `0` → Customer did not purchase
- `1` → Customer purchased

---

# 📂 Dataset Information

**Dataset:** Social Network Ads Dataset

### Features:

| Feature | Description |
|---|---|
| Age | Customer age |
| Estimated Salary | Customer estimated annual salary |

### Target:

| Target | Meaning |
|---|---|
| Purchased | Purchase decision |

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 🔍 Machine Learning Workflow

The complete workflow followed:

1. Data Understanding
2. Exploratory Data Analysis (EDA)
3. Data Preprocessing
4. Feature Scaling
5. Train-Test Split
6. Building KNN Classification Model
7. Hyperparameter Tuning using Cross Validation
8. Model Evaluation
9. ROC-AUC Analysis
10. Prediction on New Data

---

# 📊 Exploratory Data Analysis

Performed analysis to understand customer purchasing patterns:

- Distribution analysis
- Feature relationship analysis
- Purchase behavior based on age and salary
- Data visualization using plots

Key observation:

- Customers with higher age and estimated salary showed a higher tendency to purchase.

---

# ⚙️ Data Preprocessing

## Feature Scaling

Since KNN is a **distance-based algorithm**, feature scaling is necessary.

StandardScaler was applied to transform features into a comparable range, ensuring that Age and Estimated Salary contribute equally during distance calculation.

---

# 🤖 Model Development

## Baseline Model

Initial KNN model was trained with:

```
K = 5
```

Performance:

- Accuracy: ~90%

This model was considered as the baseline model.

---

# 🔎 Hyperparameter Tuning

To find the optimal number of neighbors, cross-validation was performed.

Best Parameter:

```
Best K = 9
```

Best Cross-Validation Accuracy:

```
90.62%
```

The tuned model showed better generalization compared to the baseline model.

---

# 📈 Final Model Performance

## KNN Model (K = 9)

### Accuracy

```
93.75%
```

### Confusion Matrix

```
[[48  4]
 [ 1 27]]
```

### Classification Report

| Class | Precision | Recall | F1-score |
|---|---|---|---|
| 0 | 0.98 | 0.92 | 0.95 |
| 1 | 0.87 | 0.96 | 0.92 |

---

# 📉 ROC-AUC Evaluation

ROC-AUC Score:

```
0.968
```

The high ROC-AUC score indicates that the model has excellent ability to distinguish between customers who are likely to purchase and customers who are unlikely to purchase across different classification thresholds.

---

# 🔮 Prediction on New Customer Data

The trained model can predict purchase behavior for unseen customers by providing:

- Age
- Estimated Salary

Example:

Input:

```
Age = 45
Estimated Salary = 90000
```

Output:

```
Customer is likely to purchase
```

---

# 💡 Key Learnings & Insights

- Feature scaling is essential for distance-based algorithms like KNN.
- Selecting the correct K value significantly impacts model performance.
- Cross-validation helped identify the optimal neighborhood size.
- The final KNN model achieved strong accuracy and excellent classification performance.
- ROC-AUC evaluation confirmed the model's ability to separate both classes effectively.

---

# 📁 Repository Structure

```
Social-Network-Ads-Purchase-Prediction-KNN
│
├── Dataset
│   └── Social_Network_Ads.csv
│
├── Notebook
│   └── KNN_Model.ipynb
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 Conclusion

The KNN model successfully predicts customer purchase behavior using social media advertisement data.

Through feature scaling and hyperparameter optimization, the final model achieved improved performance with **93.75% accuracy and 0.968 ROC-AUC score**, making it a reliable classification model for customer targeting analysis.

---
