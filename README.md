# Vehicle Price Prediction Using Machine Learning

## Project Overview

This project implements an end-to-end Machine Learning regression system to predict vehicle selling prices based on vehicle characteristics.

The project was completed as part of the **Devixco Solutions AI/ML Internship – Week 3, Task 03**.

It covers data cleaning, exploratory data analysis, feature engineering, preprocessing, model development, evaluation, hyperparameter optimization, feature importance analysis, and model saving.

## Dataset

The project uses the CarDekho Vehicle Price Prediction dataset obtained from Kaggle.

**Dataset Details:**
- Original Records: 8,128
- Original Features: 13
- Final Cleaned Records: 6,907
- Target Variable: `selling_price`
- Problem Type: Regression

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

## Project Workflow

### 1. Data Collection
Imported the vehicle dataset and inspected its structure.

### 2. Data Cleaning
- Removed duplicate records.
- Handled missing values.
- Converted mileage, engine, and max_power into numerical values.
- Extracted vehicle brands.
- Removed unnecessary columns.

### 3. Exploratory Data Analysis
Analyzed vehicle prices, fuel types, transmission types, ownership, and vehicle brands.

### 4. Feature Engineering
Extracted the vehicle brand from the vehicle name and selected relevant numerical and categorical features.

### 5. Data Preprocessing
- Median imputation.
- Most frequent imputation.
- StandardScaler.
- OneHotEncoder.
- Leakage-free Scikit-learn Pipeline.

### 6. Model Development

The following regression algorithms were implemented:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

### 7. Model Evaluation

Models were evaluated using:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### 8. Hyperparameter Optimization

RandomizedSearchCV and 5-fold cross-validation were used to optimize the Random Forest model.

### 9. Feature Importance

Analyzed feature importance using the optimized Random Forest model.

### 10. Model Saving

The optimized model was saved using Joblib for future predictions.

## Model Performance

Results obtained after leakage-free preprocessing:

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Random Forest | 73,510.02 | 130,176.29 | 0.9227 |
| Gradient Boosting | 82,874.18 | 131,431.44 | 0.9212 |
| Decision Tree | 93,950.90 | 171,722.55 | 0.8655 |
| Linear Regression | 133,098.56 | 261,924.59 | 0.6872 |

**Best Baseline Model:** Random Forest Regressor

## Model File

The optimized model is saved as:

`best_vehicle_price_model.joblib`

It contains the trained preprocessing and prediction pipeline.

## Results

The project successfully demonstrates an end-to-end regression workflow for predicting vehicle selling prices.

Random Forest achieved the best baseline R² score of 0.9227 among the four evaluated models.

## Limitations

- Vehicle prices can change with market conditions.
- Some original dataset values were missing.
- The dataset may not represent current vehicle market prices.
- Predictions depend on the quality of input data.

## Future Improvements

- Use more recent vehicle price data.
- Add additional vehicle-related features.
- Explore more regression algorithms.
- Develop a Streamlit-based prediction application.

## Author

**Yusra Komal**

GitHub: [Its-yusra](https://github.com/Its-yusra/Devixo-Solutions-Task-03.git))

## Internship

Devixco Solutions – AI/ML Internship

**Week 3 – Task 03: End-to-End Machine Learning Project**
