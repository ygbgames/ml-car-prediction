# ml-car-prediction

# What drives the price of a car?

This project explores a dataset of used cars to understand the factors influencing their prices and to build a predictive model. The analysis follows the CRISP-DM methodology, covering business understanding, data understanding, data preparation, modeling, and evaluation.

## Project Overview

This notebook analyzes a [dataset](https://github.com/ygbgames/ml-car-prediction/blob/main/data/vehicles.csv) of used cars, aiming to identify key price drivers and provide clear recommendations to a used car dealership on consumer preferences. We predict car prices using various machine learning models and determine which features are most influential.

## Table of Contents

-   [Business Understanding](#business-understanding)
-   [Data Understanding](#data-understanding)
-   [Data Preparation](#data-preparation)
-   [Modeling](#modeling)
-   [Evaluation](#evaluation)
-   [Deployment (Summary & Recommendations)](#deployment)

## Business Understanding

The primary goal is to predict used car prices and identify impactful features. Initial hypotheses suggest year, mileage, and manufacturer as major drivers.

## Data Understanding

Exploratory Data Analysis (EDA) was performed to understand data distributions across manufacturers, conditions, transmissions, cylinders, years, and price ranges. Outliers and missing data were identified.

## Data Preparation

Key steps included:
-   Removing entries with zero price.
-   Handling missing values and duplicates.
-   Removing low-data manufacturers (e.g., Ferrari, Aston-Martin).
-   Dropping irrelevant columns (`VIN`, `size`, `type`, `state`, `region`, `paint_color`, `drive`, `id`, `model`).
-   Extracting numeric cylinder values.
-   Converting 'year' and 'odometer' to integer types.
-   One-hot encoding categorical features.
-   Splitting the data into training and testing sets.

## Modeling

Three regression models were developed and evaluated:
1.  **Linear Regression**
2.  **Ridge Regression**
3.  **Random Forest Regressor**

## Evaluation

The models were evaluated using Root Mean Squared Error (RMSE) and R-squared (R2 Score).
-   Linear Regression: RMSE ~9987, R2 ~0.42
-   Ridge Regression: RMSE ~9987, R2 ~0.42
-   **Random Forest Regressor: RMSE ~5110, R2 ~0.85**

The Random Forest Regressor significantly outperformed the linear models.

## Deployment (Summary & Recommendations)

**Technical Key Observations:**
1.  `Year`, `odometer`, and `cylinders` are the most significant features for price prediction. Other factors like `fuel_gas` and `transmission_other` also play a role.
2.  Extensive data cleaning, including outlier removal and handling missing values, was crucial for model performance.
3.  The Random Forest model provides the best performance for price prediction.

**Business Values & Recommendations:**
1.  **Pricing Strategy:** Dealerships should heavily consider a car's **year, mileage, manufacturer, and number of cylinders** when determining prices.
2.  **Market Trends:** Newer cars consistently command higher values.
3.  **Vehicle Condition:** Good condition directly impacts price, emphasizing the importance of maintenance and reconditioning.
4.  **Inventory Management:** Stocking cars with lower odometer readings can lead to higher sales.

[Open in Google Colab](https://colab.research.google.com/github/ygbgames/ml-car-prediction/blob/main/prompt_II.ipynb)
