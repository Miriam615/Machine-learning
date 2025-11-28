# **How to select model**
How to select model depends on your data type, for supervised study, there are two types -- regression and classification.

## If your y (dependent variable) is numeric -- Regression
- e.g. concentration, bacteria amount, peak intensity, yield
### 1. If you suspect the relationship is linear -- **Linear regression**
  - **OLS** the most common, always fast, and especially good for small dataset
  - Use **PLS** instead of **OLS** if your **feature number (p) >> sample number (N)**
  - Use **Ridge** if your **OLS** has unstable coefficient, **overfitting**, or your **features have high similarities** (for example sometimes some bacteria behave very similar), but you don't wanna exclude any of them

### 2. If you need a **explanation** for your questions (for example, which bacteria affect this biomarker the most) -- **Linear regression**
  - It provides p-value, coefficient (can make coefficient plot), feature ranking

### 3. If after plotting the linear regression, the linear relationship is not strong -- **Random Forest Regressor**，**XGBoost**
  
### 4. Depends on datasize
  - **<500**: OLS, PLS, Ridge
  - **500-50,000**: Random forest, XGBoosting
  - **>50,000**: LightGBM


## If your y is a class (a group of something) -- Classification

