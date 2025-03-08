# London Property Price Prediction - Machine Learning Analysis

## Overview
This repository contains an in-depth analysis and machine learning model selection for predicting property prices in London. The project is based on the **London Property Listings Dataset** and follows a structured pipeline from **data preprocessing** to **model evaluation**.

## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Machine Learning Models](#machine-learning-models)
- [Results & Model Performance](#results--model-performance)
- [Limitations & Future Work](#limitations--future-work)
- [How to Use](#how-to-use)
- [Dependencies](#dependencies)

## Introduction
Accurately predicting real estate prices is crucial for property buyers, investors, and policymakers. This project implements and evaluates multiple **regression models** to predict London property prices based on features such as property type, size, area, and price category.

## Data Preprocessing
The dataset underwent several preprocessing steps to ensure data quality and optimal model performance:
- Handling missing values (no missing values detected)
- Feature transformation (log transformation for skewed numerical features)
- Encoding categorical variables using **Label Encoding**
- Removing redundant features to avoid multicollinearity

## Exploratory Data Analysis (EDA)
The dataset was analyzed using various **visualizations**:
- **Distributions of numerical features** (histograms and KDE plots)
- **Price variation across different property types, areas, and categories** (bar plots)
- **Correlation matrix** to understand feature relationships

## Feature Engineering
- **Feature selection**: Redundant features like `Postcode`, `Bathrooms`, and `Area` were removed.
- **Feature scaling**: Log transformation applied to `Price`, `Size`, and `Area_Avg_Price`.

## Machine Learning Models
The following machine learning models were implemented and compared:
1. **Linear Regression** (Baseline model)
2. **Polynomial Regression** (Captures non-linearity)
3. **Support Vector Regression (SVR)** (Handles complex relationships)
4. **Decision Tree Regression** (Interpretable but prone to overfitting)
5. **Random Forest Regression** (Best balance between complexity and performance)

## Results & Model Performance
Model performance was evaluated using **Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R² score**.

| Model                 | Train R² | Test R²  |
|-----------------------|---------|---------|
| Linear Regression     | 0.41    | 0.41    |
| Polynomial Regression | 0.88    | 0.81    |
| SVR                  | 0.48    | 0.49    |
| Decision Tree        | 0.94    | 0.84    |
| Random Forest        | **0.92** | **0.87** |

- **Random Forest Regression** performed best, achieving the highest R² score with minimal overfitting.

## Limitations & Future Work
- **Class imbalance** in price categories may have affected model predictions.
- **Feature selection trade-offs**: Some potentially useful interactions were removed.
- **Computational costs**: More complex models like Random Forest and SVR require higher processing power.
- **Future Improvements**:
  - Hyperparameter tuning for better performance
  - Exploring alternative models like **XGBoost, LightGBM, and Neural Networks**
  - Incorporating additional features like market trends or neighborhood development indices

## How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/London_Property_ML_Analysis.git
   cd London_Property_ML_Analysis
