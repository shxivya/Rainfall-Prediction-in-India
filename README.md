# Rainfall Prediction System

This project focuses on predicting rainfall in seven major cities across India. Using historical weather data, we aim to forecast both the likelihood of rain tomorrow (binary classification) and the estimated amount of rain (regression). This prediction system has potential applications in agriculture, infrastructure planning, and climate studies by helping users prepare for weather conditions based on data-driven insights.

## Table of Contents
1. [Objective](#objective)
2. [Dataset](#dataset)
3. [Features and Functionalities](#features-and-functionalities)
4. [Modeling Approach](#modeling-approach)
5. [Evaluation Metrics](#evaluation-metrics)
6. [Observations](#observations)
7. [Possible Future Enhancements](#possible-future-enhancements)
8. [Contributing](#contributing)

---

## Objective

The main objective of this project is to build a rainfall prediction system that uses historical weather data to predict:
1. **Rain Tomorrow (Classification)** - Predict if it will rain the next day.
2. **Rain Amount Tomorrow (Regression)** - Estimate the amount of rain expected the next day.

These predictions are useful for stakeholders in agriculture, urban planning, and individuals relying on accurate forecasts for decision-making.

## Dataset

The dataset comprises historical weather data (2010–2024) for seven cities across India: Delhi, Mumbai, Chennai, Bhopal, Jodhpur, Kolkata, and Guwahati. 

The dataset provides the basis for training and evaluating both classification and regression models.

The weather data used in this project can be accessed [here on Kaggle](https://www.kaggle.com/datasets/mukeshdevrath007/indian-5000-cities-weather-data/data).

## Features and Functionalities

### 1. Rain Tomorrow Prediction (Binary Classification)
   - **Objective**: Predict if it will rain tomorrow (yes/no).
   - **Target Variable**: `rain_tom`
   - **Model**: Random Forest Classifier

### 2. Rain Amount Prediction (Regression)
   - **Objective**: Estimate the amount of rainfall for tomorrow (in mm).
   - **Target Variable**: `rain_amount_tom`
   - **Model**: Random Forest Regressor

### 3. Data Preprocessing
   - **Feature Engineering**: Time-based features like `year`, `month`, and `day` are extracted.
   - **Feature Selection**: Unimportant or highly correlated features, such as wind speed and pressure, are removed.

### 4. Visualizations
   - **Correlation Heatmap**: Visualizes relationships between features.
   - **Scatter Plot (Actual vs. Predicted)**: Assesses regression model performance by comparing predicted and actual rain amounts.

## Modeling Approach

1. **Random Forest Classifier**: Used for predicting the binary outcome of whether it will rain tomorrow.
2. **Random Forest Regressor**: Used for predicting the continuous outcome of the rain amount.

Both models are evaluated on a hold-out test set to ensure their reliability and generalizability.

## Evaluation Metrics

- **Classification Model**: Evaluated using **accuracy**, **precision**, **recall**, and **F1-score** to account for potential class imbalance.
- **Regression Model**: Evaluated using **Mean Squared Error (MSE)**, measuring the average squared difference between actual and predicted values.

## Observations

During model evaluation, several observations were noted:
- **Classification Accuracy** was high, particularly in cities with stable weather patterns.
- **Regression Model Performance** showed moderate success, with challenges in accurately predicting the exact amount of rain during dry spells or erratic weather.
- **Feature Importance Analysis** identified temperature, humidity, and precipitation as critical features, while wind speed and pressure had minimal impact.
- **Data Imbalance** could affect binary classification due to a higher prevalence of non-rain days.

## Possible Future Enhancements

1. **Multiclass Rain Prediction**: Extend the binary classification to predict different intensities of rainfall (e.g., light, moderate, heavy).
2. **Forecasting Multiple Days**: Enable the model to predict rainfall for several days in advance.
3. **Geographical Expansion**: Collect and integrate data from additional cities and rural areas to increase model applicability.
4. **Hyperparameter Optimization**: Apply GridSearchCV or RandomizedSearchCV to fine-tune the model hyperparameters.
5. **Real-time Data Integration**: Connect to a live weather API to provide dynamic, up-to-date forecasts.
6. **User Interface**: Develop a simple web or mobile application for users to get easy access to rainfall predictions.

## Contributing

We welcome contributions to improve this project! If you’re interested in contributing, please fork the repository and make a pull request, or open an issue if you have a bug report or feature request.

