# Bitcoin-market-price-prediction-using-Supervised-Learning

This Python script focuses on Bitcoin price prediction analysis using machine learning techniques. It covers the following steps:

1. **Data Import and Exploration:**

   - Imports necessary libraries including NumPy, Pandas, Matplotlib, and Seaborn.
   - Reads data from 'bitcoin_dataset.csv' into a Pandas DataFrame (`df`).
   - Displays the first few rows of the dataset with `df.head()`.
   - Provides an overview of the dataset using `df.info()`.
   - Calculates summary statistics using `df.describe()`.
   - Computes the correlation matrix with `df.corr()`.

2. **Exploratory Data Analysis (EDA):**

   - Identifies highly correlated features with Bitcoin market price.
   - Visualizes correlations using scatterplots.
   - Checks for outliers and missing values.

3. **Data Preprocessing:**

   - Handles missing values by filling them with the mean value.
   - Converts categorical data (e.g., 'Date') into continuous data using one-hot encoding.
   - Drops the original 'Date' column.
   - Concatenates the one-hot encoded data with the original DataFrame to create a final dataset (`fin_df`).

4. **Model Building:**

   - Splits the dataset into training and testing sets.
   - Applies feature scaling using StandardScaler.
   - Builds an AdaBoostRegressor model for Bitcoin price prediction.
   - Makes predictions and calculates the Root Mean Squared Error (RMSE).

5. **Hyperparameter Tuning:**

   - Attempts to optimize the model further by using Support Vector Regressor (SVR).
   - Defines a parameter grid for hyperparameter tuning.
   - Utilizes GridSearchCV to find the best hyperparameters.

6. **Feature Importance:**

   - Examines feature importance using the AdaBoostRegressor model.
   - Visualizes the importance of features.
   - Concludes that 'BTC Market Capital' is the most important feature.

7. **Predicting Bitcoin Price:**

   - Employs Ridge Regression (ElasticNet with L1 ratio of 1) for Bitcoin price prediction.
   - Determines the current Bitcoin market capitalization and predicts the Bitcoin market price.

8. **Conclusion:**

   - Concludes that Ridge Regression (L1 ratio of 1) provides a reliable prediction model for Bitcoin market prices.
