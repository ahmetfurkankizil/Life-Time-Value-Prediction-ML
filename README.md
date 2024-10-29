## Lifetime Value (LTV) Prediction Using Regression Models

This project aims to predict Lifetime Value (LTV) based on initial user engagement data from their first session and first day. The objective is to train various regression models using both time series and train-test splitting techniques, enabling more accurate prediction of user LTV based on early engagement metrics.

Project Overview

The primary goal of this project is to build regression models that can predict the LTV of users using their initial interaction data. The project leverages data split techniques and multiple regression models to predict LTV based on user engagement during the first day and first session.

Key Features:
Data Filtering: Filters out irrelevant columns from the dataset using regular expressions.
Target Variable: The LTV column, representing the lifetime value, serves as the target for prediction.
High Correlation Removal: To improve model stability, features with a correlation above 0.8 are removed.

Splitting Methods:
Time Series Splitting: Uses a TimeSeriesSplit to retain the temporal aspect of the data.
Train-Test Splitting: Randomly splits the data, assuming no time dependencies.

Data Summary:
FirstSession_LTVNumeric: 18,583 rows, 233 columns
FirstDay_LTVNumeric: 18,718 rows, 452 columns

## Model Training and Evaluation

The following regression models are implemented:
Random Forest Regressor
Decision Tree Regressor
LightGBM (LGBM) Regressor

Each model is evaluated on the following metrics:
R2 Score: Measures goodness-of-fit.
Mean Squared Error (MSE): Indicates average squared prediction errors.
Mean Absolute Error (MAE): Reflects average absolute prediction errors.

Results Summary:
The project evaluates model performance across both splitting techniques, with a detailed comparison of R2, MSE, and MAE metrics for each model. Generally, the LGBM Regressor demonstrates the highest performance, particularly in time-series split, while Decision Tree Regressor shows the lowest performance overall.

Conclusion:
The LGBM Regressor consistently performs best across both test-train and time-series splits, especially excelling with sequential data. This model is recommended for applications that rely on accurate LTV prediction based on early user data.

Dependencies:
Python 3.x
Libraries: pandas, numpy, scikit-learn, lightgbm