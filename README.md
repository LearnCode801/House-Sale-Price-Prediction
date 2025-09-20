# House Price Prediction Model

![Project Demo](https://github.com/LearnCode801/House-Sale-Price-Prediction/blob/main/Screenshot%202024-10-30%20133822.png)

A comprehensive machine learning project for predicting house prices using the King County House Sales dataset. This project implements multiple regression algorithms with feature engineering, outlier detection, and hyperparameter tuning to achieve optimal prediction accuracy.

## 🎬 Project Demo

[![Project Demo Video](https://img.shields.io/badge/Watch-Demo%20Video-red?style=for-the-badge&logo=youtube)](https://lnkd.in/p/dmW-2Tyc)

## 📓 Project Notebook

[![View Notebook](https://img.shields.io/badge/View-Jupyter%20Notebook-orange?style=for-the-badge&logo=jupyter)](https://github.com/LearnCode801/House-Sale-Price-Prediction/blob/main/FSDS_Sales_Forcast.ipynb)

## 📊 Project Overview

This project analyzes and predicts house prices based on various property features such as location, size, condition, and amenities. The model achieved an **83.47% accuracy** using XGBoost regression with carefully selected features.

## 🎯 Key Features

- **Multiple ML Algorithms**: Comparison of 16+ regression models
- **Advanced Feature Engineering**: Creation of house age and renovation age features
- **Outlier Detection**: Multiple techniques including Z-Score, IQR, and Isolation Forest
- **Correlation Analysis**: Removal of highly correlated features (>0.8 correlation)
- **Feature Selection**: XGBoost feature importance analysis for optimal model performance
- **Hyperparameter Tuning**: Grid search optimization for best model parameters

## 📈 Dataset Information

**Source**: King County House Sales Dataset  
**Records**: 21,613 house sales  
**Features**: 21 original features (reduced to 9 key features)  
**Target Variable**: House price (USD)

### Original Features:
- `id`: Unique identifier
- `date`: Sale date
- `price`: Sale price (target variable)
- `bedrooms`: Number of bedrooms
- `bathrooms`: Number of bathrooms
- `sqft_living`: Living area square footage
- `sqft_lot`: Lot size square footage
- `floors`: Number of floors
- `waterfront`: Waterfront property (0/1)
- `view`: Quality of view (0-4)
- `condition`: Property condition (1-5)
- `grade`: Overall grade (1-13)
- `sqft_above`: Above ground square footage
- `sqft_basement`: Basement square footage
- `yr_built`: Year built
- `yr_renovated`: Year renovated
- `zipcode`: ZIP code
- `lat`: Latitude
- `long`: Longitude
- `sqft_living15`: Living area of nearest 15 neighbors
- `sqft_lot15`: Lot size of nearest 15 neighbors

## 🔧 Data Preprocessing

### Feature Engineering
- **House Age**: `age = sale_year - year_built`
- **Renovation Age**: `renov_age = |year_renovated - year_built|`
- **Date Formatting**: Extracted year from sale date

### Data Cleaning
- Handled missing values (filled with 0)
- Removed highly correlated features (correlation > 0.8)
- Applied multiple outlier detection methods

### Outlier Detection Methods
1. **Interquartile Range (IQR)**: Identified 1,146 outliers
2. **Z-Score Method**: Identified 406 outliers (threshold = 3)
3. **Isolation Forest**: Advanced anomaly detection

## 🤖 Machine Learning Models

### Models Tested:
1. **Linear Regression** - 60.51% accuracy
2. **Ridge Regression** - 60.51% accuracy
3. **Lasso Regression** - 60.51% accuracy
4. **Bayesian Ridge** - 60.51% accuracy
5. **ElasticNet** - 55.01% accuracy
6. **SGD Regressor** - 60.45% accuracy
7. **Huber Regressor** - 60.03% accuracy
8. **RANSAC Regressor** - 48.74% accuracy
9. **Gradient Boosting** - 75.99% accuracy
10. **AdaBoost** - 39.48% accuracy
11. **Extra Trees** - 74.90% accuracy
12. **Random Forest** - 77.56% accuracy
13. **Bagging** - 75.36% accuracy
14. **K-Neighbors** - 64.24% accuracy
15. **Decision Tree** - 56.02% accuracy
16. **XGBoost** - 75.99% accuracy

### Best Model: XGBoost
- **Final Accuracy**: 83.47%
- **Hyperparameters**:
  - Learning Rate: 0.1
  - Max Depth: 4
  - N Estimators: 1000

## 📊 Feature Importance

Top 9 most important features selected for final model:
1. `sqft_lot` - Lot size
2. `sqft_living15` - Living area of neighbors
3. `age` - House age
4. `zipcode` - Location (ZIP code)
5. `bathrooms` - Number of bathrooms
6. `bedrooms` - Number of bedrooms
7. `renov_age` - Renovation age
8. `floors` - Number of floors
9. `waterfront` - Waterfront property

## 📊 Model Performance

| Metric | Value |
|--------|-------|
| **R² Score** | 0.8347 |
| **Accuracy** | 83.47% |
| **Training Method** | 7-Fold Cross Validation |
| **Final Features** | 9 selected features |

## 🔍 Key Insights

1. **Location Matters**: ZIP code is a crucial factor in price prediction
2. **Size Impact**: Square footage (lot and living area) significantly affects price
3. **Age Factor**: House age shows negative correlation with price
4. **Neighborhood Effect**: Living area of nearby houses influences price
5. **Feature Reduction**: Model performance improved by removing highly correlated features

---

⭐ **Star this repository if you found it helpful!** ⭐
