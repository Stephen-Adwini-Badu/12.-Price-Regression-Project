# Price Regression Project

## Overview
This project involves conducting a comprehensive price regression analysis with the aid of sophisticated machine learning techniques. The aim is to develop accurate predictive models for estimating housing prices. The project encompasses data preprocessing, feature engineering, and rigorous model evaluation methods to ensure reliable predictions.

---

## Objectives
1. **Data Exploration**: Understand dataset structure, identify missing values, and derive meaningful insights.
2. **Feature Engineering**: Prepare data by encoding categorical variables, filling missing values, and scaling features as needed.
3. **Model Development**: Train and evaluate ensemble regression models for price prediction.
4. **Visualization**: Interpret results through regression plots and feature importance visualizations.
5. **Prediction**: Generate predictions for a test dataset and prepare submission files.

---

## Methodology
The notebook is organized into the following steps:

### 1. **Data Loading and Exploration**
- Import the dataset using Pandas.
- Perform initial exploration:
  - Check for missing values and duplicates.
  - Review dataset structure and summary statistics.

### 2. **Feature Engineering**
- Encode categorical variables using custom mapping.
- Handle missing values by imputing with mean values.
- Split data into training and testing sets.

### 3. **Model Training**
- Train ensemble regressors:
  - **AdaBoost with RandomForestRegressor**
  - **AdaBoost with GradientBoostingRegressor**
  - **AdaBoost with XGBoostRegressor**
- Optimize parameters and fit models to training data.

### 4. **Model Evaluation**
- Evaluate models using:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - Mean Absolute Percentage Error (MAPE)
  - R-squared (R²)

<table align="center">
 <tr>
   <th>MODEL</th>
   <th>MAE</th>
   <th>MSE</th>
   <th>MAPE</th>
   <th>R²</th>
 </tr>
 <tr>
   <td>Random Forest Regressor</td>
   <td align="center">16481.799</td>
   <td align="center">748898123.0</td>
   <td align="center">0.090703</td>
   <td align="center">0.865105</td>
 </tr>
 <tr>
   <td>Gradient Boosting Regressor</td>
   <td align="center">18049.904</td>
   <td align="center">808275129.0</td>
   <td align="center">0.098866</td>
   <td align="center">0.867677</td>
 </tr>
 <tr>
   <td>X Gradient Boosting Regressor</td>
   <td align="center">15938.766</td>
   <td align="center">734109206.0</td>
   <td align="center">0.086630</td>
   <td align="center">0.870763</td>
 </tr>
</table>

- Visualize regression results using Seaborn regression plots.

![1 1](https://github.com/user-attachments/assets/4c86ade3-b448-4d64-ad72-4d3e80f80215)

### 5. **Feature Importance Analysis**
- Calculate and visualize feature importance for each model.

![1 2](https://github.com/user-attachments/assets/2b81ce05-e410-438f-8727-0f5a833670ac)

### 6. **Prediction and Submission**
- Predict house prices for test data using the trained models.
- Save predictions in a CSV file for submission.

---

## Key Features
- **Data Handling**: Robust preprocessing techniques, including encoding and imputation.
- **Model Diversity**: Implementation of multiple ensemble learning regressors.
- **Performance Metrics**: Comprehensive evaluation using industry-standard metrics.
- **Visualization**: Regression plots and feature importance bar charts for model interpretation.
