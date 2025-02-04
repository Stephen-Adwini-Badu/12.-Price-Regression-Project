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
- Observations:
  - A significant number of nan values in the dataset. However in the case of the columns tabled: <p>

     <table align="center">
      <tr>
       <th></th>
       <th></th>
       <th></th>
       <th></th>
      </tr>
      <tr>
       <td>Alley</td>
       <td>BsmtQual</td>
       <td>BsmtCond</td>
       <td>BsmtExposure</td>
     </tr>
     <tr>
       <td>BsmtFinType1 &emsp;&emsp;&emsp;</td>
       <td>BsmtFinType2&emsp;&emsp;&emsp;</td>
       <td>FireplaceQu&emsp;&emsp;&emsp;</td>
       <td>GarageType&emsp;&emsp;&emsp;</td>
     </tr>
     <tr>
       <td>GarageFinish</td>
       <td>GarageQual</td>
       <td>GarageCond</td>
       <td>PoolQC</td>
     </tr>
     <tr>
       <td>Fence</td>
       <td>MiscFeature</td>
       <td></td>
       <td></td>
     </tr>
   </table>
  
- The data description list the NaN values present as catergories *(absent housing features)* instead of as a missing or null values.  
- However this only applies to categorical values all other columns with non-categorical values are actually NaN values

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
  - R-squared (R²) <p>

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
   </table> <p>
  
  - The models performed well with the best model *(Ada Boosted X Gradient Regressor)* having a Mean Percentage Error of **~9% (8.66%)** indicating a high predictive power with minor errors

- **Regression Plots**
   - **All three models (Boosted Random Forest, Boosted Gradient Boosting, and Boosted X Gradient Boosting)** exhibit **strong predictive performance**, as shown by the clustering of points around the diagonal line.

   - **No significant deviations** from the trend line suggest that **none of the models** suffers from **major biases or inconsistencies in prediction.**

 ![1 1](https://github.com/user-attachments/assets/4c86ade3-b448-4d64-ad72-4d3e80f80215)


### 5. **Feature Importance Analysis**
- With regards to feature importance the most consistently influencial feature was **OverallQual (overall material and finish)**  

- Other notables features were;  
    - **2ndFlrSF (Second floor square feet)**  
    - **GrLivArea (Above grade (ground) living area square feet)**  
    - **GarageCars (Size of garage in car capacity)**  

 ![1 2](https://github.com/user-attachments/assets/2b81ce05-e410-438f-8727-0f5a833670ac)
 
