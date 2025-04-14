# Ensemble-Learning Approach for Predictive Analytics of Driver Retention at Ola

The project applies **ensemble learning** methods to forecast driver attrition at Ola using historical driver data. Accurately identifying drivers at risk of leaving allows Ola to proactively implement retention strategies, reduce recruitment costs, and maintain operational efficiency.

---

## Problem Statement

As a data scientist at Ola, your objective is to build a machine learning model that predicts whether a driver is likely to leave the company. The dataset includes:

- **Demographics** (e.g., city, age, gender)
- **Tenure information** (e.g., joining and last working dates)
- **Performance metrics** (e.g., quarterly ratings, income, business acquired)

---

## Project Workflow

### 1. Data Exploration and Preprocessing
- Handled missing values using **KNN imputation**
- Converted date fields into appropriate formats

### 2. Feature Engineering
- Engineered features like:
  - `tenure_days`
  - `rating_change`
  - `income_change`
- Created a binary target variable `attrition`

### 3. Data Visualization and Cleaning
- Explored distributions using histograms, boxplots, and scatterplots
- Removed outliers based on IQR thresholds

### 4. Data Preparation for Modeling
- One-hot encoded categorical features
- Used **SMOTE** for class imbalance
- Standardized numerical features

### 5. Modeling and Evaluation
- Trained ensemble models:
  - **Random Forest (Bagging)**
  - **Gradient Boosting (GBM)**
  - **XGBoost**
- Tuned hyperparameters using **GridSearchCV**
- Evaluated using classification metrics and **ROC AUC**

---

## Results and Model Performance

| Model             | Accuracy | Precision | Recall | F1-Score | ROC AUC |
|------------------|----------|-----------|--------|----------|---------|
| Random Forest     | 87.6%    | 0.85      | 0.89   | 0.87     | 0.91    |
| Gradient Boosting | 88.1%    | 0.87      | 0.90   | 0.88     | 0.92    |
| XGBoost           | 89.3%    | 0.88      | 0.91   | 0.89     | 0.93    |

### Key Feature Importances
- **Tenure Duration**: Longer tenures significantly reduce attrition risk.
- **Rating Trend**: Decline in quarterly ratings is correlated with higher attrition.
- **Income Trend**: Consistent or increasing income correlates with retention.

## Insights & Recommendations
- Monitor Low-Rated Drivers: Decreasing quarterly ratings signal dissatisfaction—set up alerts or feedback loops.

- Income Support: Sudden income drops correlate with exits. Use predictive analytics to identify and intervene early.

- Reward Tenure: Loyalty incentives for long-tenured drivers could improve retention.
