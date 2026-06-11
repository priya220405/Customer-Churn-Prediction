# 📉 Customer Churn Prediction
 
![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Charts-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?logo=googlecolab)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
 
> A machine learning classification project that predicts which customers are likely to stop using a service — helping businesses take proactive retention action.
 
---
 
## 📌 Project Overview
 
Customer churn is one of the most critical business problems across telecom, banking, and subscription-based industries. Losing a customer costs **5–7x more** than retaining one.
 
This project builds a **churn prediction model** using historical customer data to identify at-risk customers before they leave.
 
Key questions answered:
- Which customers are most likely to churn?
- What features (contract type, charges, tenure) most influence churn?
- How accurately can we predict churn using classification models?
- Which model performs best — Logistic Regression or Decision Tree?
---
 
## 🗂️ Dataset
 
| Detail | Info |
|--------|------|
| Source | [Kaggle — Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) |
| Records | 7,043 customers |
| Target Column | `Churn` (Yes / No) |
| Format | CSV |
 
### Key Columns
 
| Column | Description |
|--------|-------------|
| `tenure` | Number of months with the company |
| `MonthlyCharges` | Monthly billing amount |
| `TotalCharges` | Total amount billed |
| `Contract` | Month-to-month / One year / Two year |
| `InternetService` | DSL / Fiber optic / No |
| `PaymentMethod` | Payment type used |
| `Churn` | Target — Yes (churned) / No (retained) |
 
---
 
## 🛠️ Tech Stack
 
| Tool | Purpose |
|------|---------|
| Python 3.8+ | Core language |
| Pandas | Data loading, cleaning, manipulation |
| NumPy | Numerical operations |
| Scikit-Learn | ML models, evaluation metrics |
| Matplotlib | Charts and confusion matrix |
| Seaborn | EDA visualizations |
| Google Colab | Development environment |
 
---
 
## 🔄 Project Workflow
 
```
Raw Data
   ↓
Data Loading & Exploration
   ↓
Data Cleaning & Preprocessing
   ↓
Exploratory Data Analysis (EDA)
   ↓
Feature Engineering & Encoding
   ↓
Train / Test Split (80:20)
   ↓
Model 1: Logistic Regression
Model 2: Decision Tree Classifier
   ↓
Model Evaluation (Accuracy, ROC-AUC, Confusion Matrix)
   ↓
Feature Importance Analysis
   ↓
Business Insights & Recommendations
```
 
---
 
## 📊 Visualizations
 
| # | Chart | Insight |
|---|-------|---------|
| 1 | Churn Distribution (Pie) | ~26% of customers churned |
| 2 | Churn by Contract Type (Bar) | Month-to-month contracts churn most |
| 3 | Churn by Internet Service (Bar) | Fiber optic users churn more |
| 4 | Tenure vs Churn (Histogram) | New customers churn faster |
| 5 | Monthly Charges vs Churn (Boxplot) | Churned users pay higher monthly fees |
| 6 | Correlation Heatmap | Tenure and TotalCharges are highly correlated |
| 7 | Confusion Matrix — Logistic Regression | Visual of TP, TN, FP, FN |
| 8 | Confusion Matrix — Decision Tree | Visual comparison with LR |
| 9 | ROC Curve Comparison | AUC score comparison |
| 10 | Feature Importance (Decision Tree) | Contract and tenure are top predictors |
 
---
 
## 🤖 Models Used
 
### 1. Logistic Regression
- Simple, interpretable linear classifier
- Works well for binary classification (Churn: Yes/No)
- Good baseline model
### 2. Decision Tree Classifier
- Non-linear model — captures complex patterns
- Provides feature importance scores
- Easier to explain to non-technical stakeholders
---
 
## 📈 Model Results
 
| Metric | Logistic Regression | Decision Tree |
|--------|-------------------|---------------|
| Accuracy | ~80% | ~78% |
| ROC-AUC | ~0.84 | ~0.78 |
| Precision (Churn) | ~65% | ~60% |
| Recall (Churn) | ~55% | ~62% |
 
> ✅ Logistic Regression performed better overall with higher ROC-AUC score.
 
*Note: Actual values will vary slightly based on random state.*
 
---
 
## 🔍 Key Findings
 
- 📋 **Month-to-month contract** customers churn at the highest rate (~42%)
- 💸 Customers with **higher monthly charges** are more likely to churn
- ⏳ **New customers (tenure < 12 months)** are the highest churn risk
- 🌐 **Fiber optic internet** users churn more than DSL users
- 🔑 Top 3 churn predictors: **Contract type, Monthly Charges, Tenure**
- 💡 Customers on **2-year contracts** have the lowest churn rate (~3%)
---
 
## 💼 Business Recommendations
 
| Finding | Recommendation |
|---------|---------------|
| Month-to-month customers churn most | Offer discounts to switch to annual plans |
| High monthly charges = high churn | Introduce loyalty pricing for long-term users |
| New customers churn in first year | Create onboarding program for first 3 months |
| Fiber optic users churn more | Investigate service quality issues |
 
---
 
## 🚀 How to Run
 
### Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com)
2. Upload `churn_prediction_colab.py`
3. Download dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
4. Upload the CSV when prompted
5. Run cells top to bottom
### Local
```bash
# Clone the repo
git clone https://github.com/your-username/customer-churn-prediction
cd customer-churn-prediction
 
# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn
 
# Run
python churn_prediction.py
```
 
---
 
## 📁 Project Structure
 
```
customer-churn-prediction/
│
├── churn_prediction_colab.py    # Main ML code (Colab-ready)
├── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Dataset
├── plots/
│   ├── 01_churn_distribution.png
│   ├── 02_churn_by_contract.png
│   ├── 03_churn_by_internet.png
│   ├── 04_tenure_histogram.png
│   ├── 05_monthly_charges_boxplot.png
│   ├── 06_correlation_heatmap.png
│   ├── 07_confusion_matrix_lr.png
│   ├── 08_confusion_matrix_dt.png
│   ├── 09_roc_curve.png
│   └── 10_feature_importance.png
└── README.md
```
 
---
 
## 💡 Skills Demonstrated
 
- ✅ Data loading, cleaning, and preprocessing
- ✅ Handling missing values and data type conversion
- ✅ Label encoding and one-hot encoding for categorical features
- ✅ Exploratory Data Analysis (EDA) with business framing
- ✅ Train/test splitting with `train_test_split`
- ✅ Binary classification with Logistic Regression
- ✅ Decision Tree Classifier with feature importance
- ✅ Model evaluation — Accuracy, Precision, Recall, F1, ROC-AUC
- ✅ Confusion matrix visualization
- ✅ ROC curve plotting and AUC comparison
- ✅ Translating ML results into business recommendations
---
 
## 📚 Concepts Explained
 
### What is Churn?
Churn means a customer **stops using a product or service**. Predicting it early lets companies take action — offer discounts, improve service, or reach out proactively.
 
### Why ROC-AUC Over Accuracy?
The dataset is **imbalanced** (~74% No, ~26% Yes). A model that always predicts "No Churn" would get 74% accuracy but be useless. ROC-AUC measures how well the model **separates churners from non-churners** regardless of class imbalance.
 
### What is Feature Importance?
Decision Trees calculate which features **contribute most** to making correct predictions. High importance = strong predictor of churn.
 
---
 
## 🎓 Internship Context
 
This project was completed as part of the **Data Science Internship at Skillinfytech IT Solutions**.
 
---
 
## 👩‍💻 Author
 
**Priyadharshini**
B.Tech — Artificial Intelligence & Data Science
Velalar College of Engineering and Technology, Erode
 
[![LinkedIn](www.linkedin.com/in/priyadharshini220405)

 
