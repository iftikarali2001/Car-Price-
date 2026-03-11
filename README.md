# Car Price Prediction Using Regression Models

## Project Overview

This project develops a machine learning model to predict **used car prices** using regression techniques. The analysis explores how vehicle specifications, condition, and features influence market price.

The project applies **Linear Regression, Ridge Regression, and Lasso Regression** to evaluate predictive performance and understand the effect of regularization on model stability.

The dataset contains **15,915 car listings with 23 features**, including vehicle specifications, mileage, engine characteristics, and equipment information.

---

## Objectives

The main goals of this project are:

* Predict used car prices using regression models
* Identify the most important factors affecting vehicle price
* Evaluate the impact of **regularization techniques (Ridge and Lasso)**
* Compare model performance using standard regression metrics

---

## Dataset

The dataset contains information about used vehicles such as:

* Price
* Mileage (km)
* Age
* Horsepower (hp_kW)
* Engine displacement
* Fuel type
* Body type
* Transmission type
* Vehicle features and equipment

Total records: **15,915 vehicles**
Total features: **23 columns**

---

## Data Processing

### Data Exploration

Initial analysis was performed to understand feature distributions and identify potential patterns.

Key observations:

* The **price distribution is right-skewed**, meaning most vehicles are in the lower price range.
* Mileage and age also show skewed distributions typical for used vehicles.

### Handling Categorical Variables

Categorical features such as:

* Fuel type
* Body type
* Transmission type
* Drive chain

were encoded using **one-hot encoding**.

Multi-value feature columns (such as vehicle equipment lists) were converted into binary indicator variables.

### Feature Engineering

Several preprocessing steps were performed:

* Log transformation of the target variable (`log_price`)
* Removal of redundant columns
* Encoding categorical variables
* Feature scaling using **StandardScaler**
* Train-test split (70% training, 30% testing)

---

## Models Implemented

### 1. Linear Regression

A baseline regression model was built to predict car prices.

Performance:

* **RMSE:** ~ €2,879
* **MAE:** ~ €2,002
* **R² Score:** ~ 0.828

The model explains about **82–83% of the variance in car prices**.

---

### 2. Ridge Regression

Ridge regression introduces **L2 regularization** to reduce model complexity and stabilize coefficients.

Cross-validation was used to determine the optimal regularization parameter (alpha).

Performance:

* **RMSE:** ~ €2,876
* **MAE:** ~ €2,001
* **R² Score:** ~ 0.828

Ridge provided slightly improved stability but similar predictive performance.

---

### 3. Lasso Regression

Lasso regression applies **L1 regularization**, which can automatically remove unimportant features by shrinking their coefficients to zero.

Performance:

* **RMSE:** ~ €2,880
* **MAE:** ~ €2,002
* **R² Score:** ~ 0.828

Lasso produced a **simpler model by eliminating several features** while maintaining comparable accuracy.

---

## Model Comparison

| Model             | RMSE (€) | MAE (€) | R²    |
| ----------------- | -------- | ------- | ----- |
| Linear Regression | 2879     | 2002    | 0.828 |
| Ridge Regression  | 2876     | 2001    | 0.828 |
| Lasso Regression  | 2880     | 2002    | 0.828 |

All models achieved **very similar performance**, indicating that the baseline model already generalizes well without severe overfitting.

---

## Key Insights

Important factors that **increase car price**:

* Higher horsepower
* More gears
* Diesel fuel type
* Higher vehicle weight
* Premium features (automatic transmission, leather seats, 4WD)

Factors that **reduce car price**:

* Vehicle age
* Higher mileage
* Manual transmission

These findings align with typical patterns observed in used vehicle markets.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Project Structure

```id="5oowt1"
car-price-prediction
│
├── notebook
│   └── car_price_analysis.ipynb
│
├── report
│   └── Car_Price_report_version_2.pdf
│
├── data
│   └── Car_Price_data.csv
│
└── README.md
```

---

## Author

**Iftikar Ali**

Regression Modelling Project
Car Price Prediction Analysis
