
# 📘 Logistic Regression Case Study: Income Classification Using Census Data

## 📌 Overview

This project applies **Logistic Regression** to predict whether an individual earns **more than $50K annually** based on demographic and employment-related information. The data is derived from the 1994 U.S. Census database, consisting of ~32,000 records and over 15 features. The primary goal is to analyze how various socio-economic factors influence income classification.

---

## 📁 Dataset Description

- **Source:** 1994 U.S. Census Bureau
- **Records:** ~32,000 individuals
- **Target Variable:** `annual_income`  
  - 0 → ≤50K  
  - 1 → >50K
- **Features:** age, workclass, education, marital-status, occupation, relationship, race, sex, hours-per-week, native-country, etc.

---

## 🔍 Exploratory Data Analysis (EDA)

### 🎯 Target Distribution

| Class     | Count    | Percentage |
|-----------|----------|------------|
| ≤50K      | ~75%     | Majority   |
| >50K      | ~25%     | Minority   |

- **Observation**: Class imbalance exists; most individuals earn ≤50K.

### 🔧 Data Cleaning
- Replaced missing values (`?`) in `workclass`, `occupation`, and `native-country` with `"others"`.
- Dropped uninformative column: `fnlwgt`.

---

### 📊 Statistical Testing

#### ✅ Chi-Square Test (for Categorical Features)

| Feature           | Influential? |
|-------------------|--------------|
| workclass         | ✅ Yes       |
| education         | ✅ Yes       |
| marital-status    | ✅ Yes       |
| occupation        | ✅ Yes       |
| relationship      | ✅ Yes       |
| sex               | ✅ Yes       |
| native-country    | ✅ Yes       |
| race              | ❌ No        |

#### ✅ Z-Test (for Continuous Features)

| Feature          | Influential? |
|------------------|--------------|
| age              | ✅ Yes       |
| education-num    | ✅ Yes       |
| capital-gain     | ✅ Yes       |
| capital-loss     | ✅ Yes       |
| hours-per-week   | ✅ Yes       |

---

## ⚙️ Data Processing

- Applied **One-Hot Encoding** on relevant categorical features.
- Final dataset is fully numeric and suitable for modeling.
- Checked **multicollinearity** using **VIF** for continuous variables (all < 5).

---

## 🤖 Model Development

- **Model:** Logistic Regression (`statsmodels.api.Logit`)
- **Train-Test Split:** 80:20
- **Threshold:** 0.5 (default for binary classification)

### 🧪 Evaluation Metrics

| Metric         | Class 0 (≤50K) | Class 1 (>50K) |
|----------------|----------------|----------------|
| Precision      | 0.88           | 0.73           |
| Recall         | 0.93           | 0.60           |
| F1-Score       | 0.90           | 0.66           |
| **Accuracy**   | **85%**        |                |

- **Model Strength**: Excellent performance on majority class (≤50K)
- **Model Limitation**: Lower recall for high-income earners

---

## 📊 Business Insights

- **Education Level**: Higher education leads to higher income probability.
- **Age & Hours**: Older individuals working more hours have a higher chance of earning >50K.
- **Capital Gain/Loss**: Directly associated with high-income groups.
- **Occupation & Marital Status**: Strongly correlated with earning potential.

---

## 📂 Repository Structure

```

LogisticRegression-IncomeClassification/
├── data/
│   └── census\_income.csv
├── notebooks/
│   └── logisticregression.py
├── report.md
└── README.md

```

---

## 📬 Contact

👤 **Sahil Karande**  
🎓 Computer Engineering | CDAC DBDA  
📧 skarande220@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/sahil-karande-a77aa7207/) | [GitHub](https://github.com/sahilkarande)

---
