# California Housing Prices Dataset

## Overview
The **California Housing Prices** dataset contains summary statistics about housing districts in California, derived from the **1990 U.S. Census**. It is a classic, beginner-friendly dataset widely used to teach **machine learning fundamentals**, popularized by Aurélien Géron’s book *Hands-On Machine Learning with Scikit-Learn and TensorFlow*.

This dataset is ideal for learning how to:
- Clean and preprocess real-world data
- Perform exploratory data analysis (EDA)
- Build and evaluate regression models

---

## Key Characteristics
- Based on **1990 census data**
- Moderate size (≈20,000 rows)
- Requires **basic preprocessing** (missing values, feature scaling, encoding)
- Mix of **numerical and categorical** features
- Target variable is **continuous** (regression problem)

---

## Dataset Structure
Each row represents a **California housing district** (not an individual house).

### Target Variable
- **`median_house_value`**  
  Median house price for the district (in USD)

---

## Data Dictionary

| Column Name | Description |
|-------------|------------|
| `longitude` | Longitude of the district |
| `latitude` | Latitude of the district |
| `housing_median_age` | Median age of houses in the district |
| `total_rooms` | Total number of rooms in the district |
| `total_bedrooms` | Total number of bedrooms (contains missing values) |
| `population` | Total population in the district |
| `households` | Number of households in the district |
| `median_income` | Median household income (in tens of thousands USD) |
| `median_house_value` | Median house price (target variable) |
| `ocean_proximity` | Categorical feature indicating proximity to the ocean |

---

## Common Preprocessing Tasks
Students are expected to perform:
- Handling missing values (`total_bedrooms`)
- Feature scaling (e.g., standardization)
- Encoding categorical variables (`ocean_proximity`)
- Feature engineering (e.g., rooms per household)
- Train/test splitting

---

## Example Learning Use Cases

### Exploratory Data Analysis (EDA)
- Visualize housing prices geographically
- Analyze income vs. house value
- Detect outliers and skewed distributions

### Machine Learning
- Linear regression and regularization (Ridge, Lasso)
- Decision trees and random forests
- Model evaluation using RMSE or MAE
- Hyperparameter tuning

### Feature Engineering
- Rooms per household
- Bedrooms per room
- Population per household

### Model Interpretation
- Feature importance analysis
- Bias–variance tradeoff
- Error analysis

---

## Notes & Caveats
- Prices are **capped** at an upper limit (important for model evaluation)
- Income is **normalized**, not raw dollar values
- Represents **district-level aggregates**, not individual properties

---

## Attribution
Originally featured in:
> Pace, R. Kelley, and Ronald Barry.  
> *Sparse spatial autoregressions.* Statistics & Probability Letters, 1997.

Popularized by:
> Aurélien Géron — *Hands-On Machine Learning with Scikit-Learn and TensorFlow*


