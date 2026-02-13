 This project aims to predict residential real estate prices using various machine learning techniques. The workflow follows a standard data science pipeline, including data cleaning, exploratory data analysis (EDA), feature engineering, and hyperparameter tuning using XGBoost.

## Dataset
The dataset is from the Kaggle https://www.kaggle.com/datasets/vallabhadattap/kingcountyhousing and contains information on house sales, including features such as:

Dimensions: Square footage of living space, lot size, and basement.

Rooms: Number of bedrooms and bathrooms.

Condition: Overall grade and condition of the property.

Location: Zip code, latitude, and longitude.

Target Variable: price (The sale price of the home).

## Project Workflow
# 1. Data Cleaning & Preprocessing

Handling Inconsistencies: Removal of duplicate entries and unnecessary columns (like id).

Date Transformation: Formatting the sale date into a numerical format suitable for modeling.

Outlier Removal: Filtering extreme values (e.g., properties with an unusually high number of bedrooms).

 # 2. Exploratory Data Analysis (EDA)

Correlation Analysis: Identification of key drivers of price, such as sqft_living and grade.

Statistical Testing: Utilizing Chi-Square tests to determine dependencies between categorical features.

Visualizations: Using heatmaps and scatter plots to understand feature distributions and relationships.

# 3. Feature Engineering

Binary Encoding: Transforming features like yr_renovated into binary flags (Renovated vs. Not Renovated).

Categorical Handling: Processing categorical variables to ensure compatibility with regression algorithms.

# 4. Machine Learning Models

The project implements several algorithms to compare performance:

Linear Regression: Used as a baseline model.

K-Nearest Neighbors (KNN) Regressor: Evaluated for its performance on spatial and structural data.

XGBoost Regressor: The primary model, known for high performance on tabular data.

# 5. Hyperparameter Tuning

To optimize the XGBoost model, a Grid Search with Cross-Validation (GridSearchCV) was performed. The search explored combinations of:

n_estimators (Number of trees)

max_depth (Complexity of the trees)

learning_rate (Step size shrinkage)

# Final Performance
The final model was evaluated using R-squared and Root Mean Squared Error (RMSE) to ensure accuracy and generalizability.

# Validation R²: ~0.816

# Test R²: Results consistently showed high accuracy after addressing overfitting through cross-validation.
 Technologies Used
 Python

Pandas & NumPy: Data manipulation.

Matplotlib & Seaborn: Data visualization.

Scikit-Learn: Preprocessing and model evaluation.

# XGBoost: Advanced gradient boosting.
 This was a joint project with Aitor, Isis, and Suzana. The link to their github is below.
 https://github.com/isishassan
 https://github.com/aitor-vergaramartin
 https://github.com/suzanacracco-max
