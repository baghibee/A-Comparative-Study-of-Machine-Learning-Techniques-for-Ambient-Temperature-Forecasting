# Comparative Study of Machine Learning Techniques for Predicting Temperature over Bayfordbury
## Project Overview
### This is an MSc Data Science course project at the University of Hertfordshire. It attempts to predict ambient temperature using different Machine learning models. The study performs statistical assessments of Support Vector Regression (SVR), Ridge regression, and Lasso regression using meteorological data from the Bayfordbury weather station.
## Motivation
### Various fields, such as agriculture, energy management, and public health libraries, require accurate temperature forecasting. For instance, traditional techniques like multiple linear regressions (MLR) do not work well with non-linear weather data. In this project, I learned how state-of-the-art machine learning techniques like SVR, Ridge, and Lasso Regression can be used to make predictions more accurately by better accommodating non-linear dependencies.
## Dataset
### A dataset of daily meteorological observations was used in this project, which was gathered from the Bayfordbury weather station between 8th May 2011 and 21st May 2024. Variables within this dataset are as follows:
### •	Wind Direction
### •	Wind Speed
### •	Humidity
### •	Ambient Temperature
### •	Barometric Pressure
### •	Solar Radiation
## Data Preprocessing
### •	Cleaning: Remove non-numeric columns and then scale the data. Handle missing values, using which some columns were dropped due to excessive missing data.
### •	Aggregation: The half-hourly data was then resampled into a daily format for simpler modeling and analysis.
### •	Feature Scaling: We scaled the features using MinMaxScaler to keep all variables on the same scale for model building.
## Models Developed
## 1. Support Vector Regression (SVR)
### •	Purpose: It captures non-linear relationships in data by using kernel functions.
### •	Tuning: We used Grid Search with Cross-Validation to optimize the parameters such as C, gamma, and kernel type.
### •	Performance: The study concluded that SVR is the top-performing model, with an R² value of 0.9989. CNN also reported the lowest Mean Absolute Error (0.0694) and Root Mean Squared Error (0.1778).
## 2. Ridge Regression
### •	Purpose: To build a linear model with L2 regularization to prevent overfitting and handle multicollinearity among predictors.
### •	Tuning: Tuned the alpha parameter via Grid Search Cross-Validation.
### •	Performance: Ridge Regression gave me an R²−Value of 0.9973, Mean Absolute Error of 0.1520, and Root Mean Squared Error of 0.2750.
## 3. Lasso Regression
### •	Purpose: Like Ridge Regression, L1 regularization allows feature selection by reducing some coefficients to zero.
### •	Tuning: Optimized alpha parameter by Grid Search with Cross-Validation.
### •	Performance: Lasso Regression showed a minimum R² value of 0.9969 between the models and printed a Mean Absolute Error of 0.1485 and a Root mean squared error of 0.2949.
## Results and Discussion
### The SVR Model gives better predictive accuracy than the Ridge and Lasso Regression Models, as the R² value of the model was higher with similar Error Metrics. Ridge Regression performed well, while Lasso Regression, though it could be used for feature selection, leads a bit behind in prediction accuracy.
## Model Performance Comparison
### Model	Mean Error (ME)	Mean Absolute Error (MAE)	Root Mean Squared Error (RMSE)	R²
### SVR	-0.0057	0.0694	0.1778	0.9989
### Ridge Regression	-0.0006	0.1520	0.2750	0.9973
### Lasso Regression	0.0017	0.1485	0.2949	0.9969
## Future Work
### •	Advanced Models: Explore more advanced machine learning models such as Random Forests or Gradient Boosting Machines to improve prediction accuracy even further.
### •	Time Series Analysis: Use time series techniques like Seasonal Decomposition of the Time Series (STL) or Autoregressive Integrated Moving Average (ARIMA) to gain insights into temporal dynamics in your data.
### •	Feature Engineering: Now, consider other weather metrics and how their interactions can improve model performance.

