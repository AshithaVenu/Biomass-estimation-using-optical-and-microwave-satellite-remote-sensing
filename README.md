# Biomass Prediction: Regression Analysis

A Jupyter notebook that compares three regression approaches for predicting total biomass from ground survey data.

## What It Does

The code loads a CSV dataset, prepares features by dropping non-numeric columns and the target variable, then splits the data into 80% training and 20% testing sets. It runs three regression models on the same data:

1. **Stepwise Regression** — automatically selects the most significant features using forward-backward selection based on p-values (threshold_in = 0.01, threshold_out = 0.05). Uses statsmodels OLS.

2. **Multiple Linear Regression** — fits an OLS model using all available numeric features. Provides full statistical summary including coefficients, p-values, R-squared, and diagnostic statistics.

3. **Linear Regression (sklearn)** — fits a standard linear regression using scikit-learn. Reports coefficients and standard regression metrics.

All three models are evaluated on the test set using R², RMSE, MAE, and MSE. The code generates predicted vs. actual scatter plots, residual analysis plots, and saves prediction results and metric comparisons to CSV files.

## How to Use

1. Update the `csv_file_path` variable to point to your dataset.
2. Ensure your target column is named `Total Biomass of a plot (kg)`.
3. Run all cells in the notebook.
4. Check your working directory for output PNG and CSV files.

## Dependencies

- pandas
- numpy
- statsmodels
- scikit-learn
- matplotlib
- seaborn

