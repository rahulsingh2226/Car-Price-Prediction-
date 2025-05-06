# 🚗 Car Price Prediction Using Linear Regression

This project focuses on predicting the **selling price of used cars** using machine learning techniques. The dataset includes features such as brand, model, year, mileage, engine, transmission type, and more. We implement end-to-end data cleaning, preprocessing, feature engineering, and modeling using **Linear Regression**.

---

## 📁 Dataset

The dataset used for this project is `Car details v3.csv`, which includes various details about used cars listed for sale.

Key columns:
- Car Name
- Year
- Selling Price (target)
- Present Price
- Kms Driven
- Fuel Type
- Seller Type
- Transmission
- Owner

---

## 🔍 Project Workflow

### 1. 📦 Importing Libraries & Dataset
Standard libraries like `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn` are used.

---

python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.linear_model import LinearRegression

## 🧹 Step 1: Data Cleaning & Inspection

- Renamed columns for clarity and consistency.
- Created a helper function `car()` to:
  - Check null values
  - Display data types
  - List column names and basic info
- Dropped irrelevant columns that don’t influence the sale price.

---

## 📊 Step 2: Exploratory Data Analysis (EDA)

- Isolated numerical columns.
- Checked for outliers and skewness using:
  - `boxplot()`
  - `histplot()` from seaborn
- Cleaned columns with string-embedded numerical values:
  - `"1900 cc"` → `1900`
  - `"22 kmpl"` → `22`

---

## 🔧 Step 3: Feature Engineering

- Separated the **Make** from the combined `Make_Model` column to reduce overfitting.
- Dropped the granular `Model` information.
- Applied encoding:
  - **Label Encoding** for categorical, non-hierarchical features like fuel type and transmission.
  - **Ordinal Encoding** for hierarchical features like `Year`.

---

## 🧮 Step 4: Target Transformation

- Checked skewness in the `Selling Price` column.
- Applied **log transformation** to normalize the target distribution.

---

## 🔢 Step 5: Data Scaling & Cleanup

- Scaled numerical features using standard scaling techniques.
- Ensured all null values were removed from the dataset.

---

## 🤖 Step 6: Model Training

- Built a **Linear Regression** model using the cleaned and preprocessed dataset.
- Achieved an **R² score of 0.86**, indicating strong predictive performance.

---

## ✅ Conclusion

Key takeaways:
- Effective data preprocessing improves model accuracy significantly.
- Feature engineering (e.g., splitting make/model) helps reduce noise.
- A well-prepared dataset allows even simple models like Linear Regression to perform well.
