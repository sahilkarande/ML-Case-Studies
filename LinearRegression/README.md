# 📊 Linear Regression Case Studies: Salary & Housing Price Prediction

## 📌 Overview

This repository presents two practical case studies demonstrating the application of **Linear Regression** in real-world scenarios:

1. **Salary Prediction** – Predicting employee salaries based on their years of experience.
2. **Housing Price Prediction** – Estimating house prices using property features.

Each project includes thorough **Exploratory Data Analysis (EDA)**, model building using `scikit-learn`, and business insights drawn from the results.

---

## 📁 Project Descriptions

### 1. 💼 Salary Prediction (Simple Linear Regression)

**Objective**: Predict an employee's salary based on years of experience.

**Dataset**: `data.csv`  
**Features**:  
- `YearsExperience` (Independent)  
- `Salary` (Dependent)

**Approach**:
- Performed EDA to visualize data distribution.
- Built a linear regression model to predict salary.
- Visualized predictions with a fitted regression line.

**Key Metrics**:
- R² Score (Test): **0.71**
- MSE: ~₹39.7 Billion

📈 **Insight**: Salaries increase linearly with experience. The model is effective for mid-level career planning.

---

### 2. 🏠 House Price Prediction (Multiple Linear Regression)

**Objective**: Predict housing prices using features like square footage, location, and number of rooms.

**Dataset**: `housing.csv`  
**Features**: 19+ columns including `sqft_living`, `grade`, `bathrooms`, etc.

**Approach**:
- Cleaned dataset and dropped irrelevant features like `id` and `date`.
- Performed extensive EDA: heatmaps, boxplots, and scatter plots.
- Built a multiple linear regression model for price prediction.

**Key Metrics**:
- R² Score: **0.71**
- MSE: ~₹39.7 Billion

📈 **Insight**: House size, grade, and bathroom count are the most influential factors in determining price.

---

## 📊 Exploratory Data Analysis Highlights

### Salary Dataset:
- Most employees have 3–8 years of experience.
- Salaries are right-skewed; most earn ₹40,000–₹80,000.
- Strong positive correlation between experience and salary (**0.97**).

### Housing Dataset:
- Highly skewed price distribution due to outliers.
- Strong correlations:
  - `sqft_living` → 0.70
  - `grade` → 0.67
  - `bathrooms` → 0.53
- Price trends show strong dependency on living space and construction quality.

---

## 📌 Technologies Used

- **Python**
- **Pandas**, **NumPy**
- **Seaborn**, **Matplotlib**
- **scikit-learn** for modeling
- **Jupyter Notebook** for code and visuals

---

## ✅ Results Summary

| Project              | Model Type           | R² Score | MSE (Approx.) | Key Features                     |
|----------------------|----------------------|----------|----------------|-----------------------------------|
| Salary Prediction     | Simple Linear Reg.   | 0.71     | ₹39.7 Billion   | YearsExperience                   |
| House Price Prediction| Multiple Linear Reg. | 0.71     | ₹39.7 Billion   | sqft_living, grade, bathrooms     |

---

## 📬 Contact

👤 **Sahil Karande**  
🎓 Computer Engineering | CDAC DBDA  
📧 skarande220@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/sahil-karande-a77aa7207/) | [GitHub](https://github.com/sahilkarande)

---

<!-- ## 📂 Repository Structure

```

<!-- LinearRegression-CaseStudy/
├── data/
│   ├── data.csv
│   └── housing.csv
├── notebooks/
│   └── linearregression.py
├── images/
│   └── \[EDA & model plots]
├── report.md
└── README.md --> -->

```

