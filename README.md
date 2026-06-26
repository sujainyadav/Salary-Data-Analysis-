# 💼 Salary-Data-Analysis

## 📌 Project Overview
This project analyzes salary data of 22,000+ job records to identify key factors influencing salary such as job role, location, company rating, and employment type. It includes end-to-end EDA, data cleaning, business question analysis, and advanced future scope modules covering machine learning, time-series analysis, and geo-visualisation.

---

## 🎯 Objectives
- Analyze salary trends across different roles and cities
- Understand correlation between company rating and salary
- Identify high-paying job categories and companies
- Build and compare salary prediction models (Linear Regression, Random Forest, Gradient Boosting)
- Visualize city-level salary patterns on an interactive India map

---

## 📊 Dataset
- **Source File:** `Salary_Dataset_DSL.csv`
- **Rows:** ~22,770
- **Columns:** 8

| Feature | Description |
|---------|-------------|
| `Rating` | Company rating (numeric) |
| `Company Name` | Name of the employer |
| `Job Title` | Specific job designation |
| `Salary` | Reported salary (₹) |
| `Salaries Reported` | Number of salary reports submitted |
| `Location` | City of the job |
| `Employment Status` | Full-time / Part-time / Contract etc. |
| `Job Roles` | Broader job category |

---

## 🗺️ Project Roadmap

| Step | Section | Description |
|:----:|---------|-------------|
| 1 | 📦 Libraries | Import all required packages |
| 2 | 📂 Load Data | Read & preview the dataset |
| 3 | 🔍 EDA | Understand structure & statistics |
| 4 | 🧹 Data Cleaning | Handle nulls, duplicates & outliers (IQR method) |
| 5 | ❓ Analysis | Answer 7 business questions |
| 6 | 📈 Bonus Visuals | Job role distribution & rating trend |
| 7 | 📝 Insights | Summary & key takeaways |
| 8 | 🚀 Future Scope | Regression · ML · Time-Series · Geo-Map |

---

## 🔍 Key Insights

- **Senior / specialized roles** earn significantly higher average salaries
- **Location is the strongest predictor** — city of work has a major impact on pay
- **Weak correlation** between company rating and salary (rating alone ≠ high pay)
- **Full-time roles** consistently pay more than contract or part-time positions
- **Filtering by ≥ 20 reported salaries** surfaces the most credible high-paying companies

---

## ❓ Business Questions Answered

| # | Question |
|:--:|---------|
| Q1 | Which job role has the highest average salary? |
| Q2 | Which city offers the highest average salary? |
| Q3 | Top 5 vs Bottom 5 paying companies in New Delhi with Rating = 5 |
| Q4 | Which job title has the highest number of salaries reported? |
| Q5 | Top 10 companies with highest salary (≥ 20 reported salaries) |
| Q6 | Is there a relationship between company rating and salary? |
| Q7 | How does employment status affect salary? |

---

## 🚀 Future Scope (Implemented)

### FS1 — 📐 Multivariate Linear Regression
- Features used: `Job Roles`, `Location`, `Rating`, `Employment Status`
- Label encoding + Standard Scaling applied
- Metrics: **R² Score** and **RMSE**
- Plots: Actual vs Predicted scatter, Residual plot, Feature coefficients

### FS2 — 📅 Time-Series Salary Trend
- Auto-detects date column; falls back to synthetic monthly trend if absent
- 3-month **rolling average** applied to smooth noise
- Outputs start/end salary and % change over the period

### FS3 — 🤖 ML Models (Random Forest + Gradient Boosting)
- Features: `Job Roles`, `Location`, `Rating`, `Employment Status`, `Salaries Reported`
- 5-fold **cross-validation** for robust evaluation
- **Feature importance** ranking to identify top salary drivers
- Model comparison chart (R² side-by-side)

### FS4 — 🗺️ Geo-Visualisation (India City Map)
- **Plotly Express** interactive bubble map (city salary intensity)
- **Matplotlib** static fallback bubble chart
- Bubble size and color both encode average salary per city

---

## ⚙️ Tech Stack

| Category | Libraries |
|----------|-----------|
| Data Wrangling | `pandas`, `numpy` |
| Visualisation | `matplotlib`, `seaborn`, `plotly` |
| Machine Learning | `scikit-learn` (LinearRegression, RandomForestRegressor, GradientBoostingRegressor) |
| Utilities | `warnings` |

---

## 📁 File Structure

```
Salary-Data-Analysis/
│
├── Salary_Dataset_DSL.csv               # Raw dataset
├── Salary_Data_Analysis_Extended.ipynb  # Full notebook (EDA + Future Scope)
└── README.md                            # Project documentation
```

---

## 🔮 Further Extension Ideas

- 🔧 **Hyperparameter tuning** — GridSearchCV / RandomizedSearchCV on ensemble models
- 🧠 **Deep Learning** — MLP regressor using Keras for salary prediction
- 💬 **NLP on Job Titles** — TF-IDF / word embeddings to capture title semantics
- 🌐 **Streamlit / Dash App** — Deploy as an interactive salary prediction dashboard
- 📍 **Experience-based analysis** — Stratify salary trends by years of experience

---

*✍️ Analysis by: Sujain Yadav &nbsp;|&nbsp; 🐍 Python · Pandas · Scikit-learn · Plotly &nbsp;|&nbsp; 📁 Dataset: Salary_Dataset_DSL.csv*
