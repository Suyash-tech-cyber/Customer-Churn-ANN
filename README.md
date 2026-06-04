# Customer Churn Prediction — Banking Dataset

![Python](https://img.shields.io/badge/Python-3.13-blue) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange) ![Dataset](https://img.shields.io/badge/Dataset-Banking%20Churn-green) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview

This project builds and compares two machine learning models — **Logistic Regression** and **Random Forest** — to predict whether a bank customer will leave (churn) based on their profile and account behaviour. The workflow covers data cleaning, preprocessing, feature encoding, model training, and evaluation using standard classification metrics.

Customer churn prediction is a high-value problem in the banking and finance industry. Retaining an existing customer is significantly cheaper than acquiring a new one, making accurate churn prediction a direct business priority.

---

## Models Compared

| | Logistic Regression | Random Forest |
|---|---|---|
| **Accuracy** | ~79% | **86.65%** |
| **Precision** | Lower | **75.82%** |
| **Recall** | Lower | **47.08%** |
| **F1 Score** | Lower | **58.08%** |

**Conclusion:** Random Forest outperformed Logistic Regression across all evaluation metrics. Its ability to capture complex, non-linear patterns in customer behaviour makes it the preferred model for this problem.

---

## Project Structure

```
Customer-Churn-ANN/
├── data/
│   └── Churn_Modelling.csv         # Banking customer churn dataset
├── notebooks/
│   └── Churn_modelling.ipynb       # Full ML workflow notebook
├── images/                         # Charts and visualisations
└── README.md
```

---

## Dataset

- **Records:** 10,000 customers
- **Features:** 11 attributes including Credit Score, Geography, Gender, Age, Tenure, Balance, Number of Products, and Estimated Salary
- **Target:** Binary — whether the customer exited (1) or stayed (0)
- **Preprocessing:** Removed irrelevant columns (RowNumber, CustomerId, Surname), applied one-hot encoding to categorical features (Geography, Gender), and performed an 80/20 train/test split

---

## Technologies Used

- Python 3.13
- Scikit-learn (Logistic Regression, Random Forest, metrics)
- Pandas
- NumPy
- Matplotlib

---

## Workflow

1. **Data Loading & Inspection** — load dataset, check shape, data types, null values
2. **Data Cleaning** — removed irrelevant identifier columns
3. **Feature Encoding** — one-hot encoding for Geography and Gender using `pd.get_dummies()`
4. **Train/Test Split** — 80% training, 20% testing
5. **Logistic Regression** — baseline model, evaluated with accuracy, precision, recall, F1
6. **Random Forest** — ensemble model, evaluated with same metrics
7. **Model Comparison** — bar chart comparison of both models across all metrics

---

## Key Results

- Random Forest achieved **86.65% accuracy** compared to Logistic Regression
- Random Forest demonstrated stronger generalisation on unseen customer data
- The dataset had **no missing values**, reducing preprocessing complexity
- One-hot encoding was required to handle categorical features before model training

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/Suyash-tech-cyber/Customer-Churn-ANN.git
cd Customer-Churn-ANN

# Install dependencies
pip install scikit-learn pandas numpy matplotlib

# Open the notebook
jupyter notebook "notebooks/Churn_modelling.ipynb"
```

---

## Author

**Suyash Kharel**  
Bachelor of Information Technology — Victorian Institute of Technology  
GitHub: [@Suyash-tech-cyber](https://github.com/Suyash-tech-cyber)
