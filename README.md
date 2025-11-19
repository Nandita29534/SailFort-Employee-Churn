# 🏢 Salifort Motors — Employee Retention Analysis & Prediction

## 📌 About the Company
Salifort Motors is a fictional France-based alternative energy vehicle manufacturer with a global workforce of over 100,000 employees. The company leads in electric, solar, algae, and hydrogen-powered automotive technologies through strong vertical integration across research, design, construction, validation, and distribution.

---

## 🎯 Business Case
Senior leadership at Salifort Motors conducted an employee survey and requested a data-driven analysis to uncover factors influencing employee turnover.  
Your task as a data specialist:

- Analyze the employee dataset to identify drivers of churn  
- Build a predictive model that determines whether an employee will leave the company  
- Use relevant features such as department, project load, monthly hours, satisfaction, evaluation score, tenure, promotions, etc.

The final deliverable provides insights and a predictive model that can guide HR strategy and reduce costly employee turnover.

---

## 🧠 Key Insights from EDA

### 🔁 Duplicate Rows
- The dataset contained multiple identical rows across all columns.  
- These **do not indicate data quality issues** because many employees naturally share identical attributes.  
- With **no unique employee ID**, removing duplicates would incorrectly delete legitimate employee records.  
👉 **Decision:** Keep all duplicates to preserve the true distribution of employee patterns.

### 📉 Employee Churn Drivers
Exploratory analysis indicates employees are leaving due to **poor management and burnout**:

- High number of projects + long working hours → higher attrition  
- Low satisfaction scores strongly correlate with churn  
- Lack of promotions and lower performance evaluations contribute to turnover  
- Employees with **tenure > 6 years rarely leave**, indicating stability among senior staff  
- A large subset of employees appears to be **overworked and burned out**

---

## ⚖️ Handling Class Imbalance
- The target variable (left vs stayed) was imbalanced  
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset before model training

---

## 🤖 Models Tested
Three models were built and evaluated:

| Model | Notes |
|-------|-------|
| **Logistic Regression** | Baseline linear model |
| **Random Forest** | Strong tree-based ensemble |
| **XGBoost** | Gradient boosting model |

### 🏆 Champion Model: **Random Forest**
- Delivered the strongest overall performance  
- Captured nonlinear relationships between employee factors and churn  
- Robust against noise & overfitting

---
