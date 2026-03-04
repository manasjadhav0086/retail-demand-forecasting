# Retail Demand Forecasting Platform

## Project Overview

Retail businesses often struggle with inaccurate demand planning, which leads to **stockouts, lost revenue, and excess inventory costs**.
This project builds a **machine learning-based demand forecasting system** that predicts future product sales and helps businesses optimize inventory decisions.

The platform integrates **data engineering pipelines, machine learning forecasting models, and Power BI dashboards** to provide a complete retail analytics solution.

---

# Business Problem

Retail companies need to answer critical questions such as:

* How much product demand should be expected next week?
* Which stores generate the highest sales?
* How does seasonality affect demand?
* What inventory level should be maintained to avoid stockouts?

Without forecasting systems, companies rely on manual planning, which leads to inefficient inventory management.

This project solves this problem by building an **automated retail demand forecasting system**.

---

# Solution Architecture

Retail Sales Data
↓
Data Cleaning & Transformation
↓
Feature Engineering (Time-Series Features)
↓
Machine Learning Forecasting Model (XGBoost)
↓
Demand Predictions
↓
Power BI Business Intelligence Dashboard

---

# Dataset

Dataset used: **Walmart Store Sales Forecasting**

Files used in this project:

* train.csv – Historical weekly sales data
* features.csv – External factors such as temperature, fuel price, and unemployment
* stores.csv – Store metadata including store type and size

Key columns used:

Store
Department
Date
Weekly_Sales
IsHoliday
Temperature
Fuel_Price
CPI
Unemployment

---

# Tech Stack

### Programming

Python
Pandas
NumPy

### Machine Learning

Scikit-learn
XGBoost

### Data Visualization

Matplotlib
Seaborn
Power BI

### Data Processing

Time-series feature engineering
Lag features
Rolling averages

---

# Project Structure

```
retail-demand-forecasting
│
├── data
│   ├── raw
│   │   ├── train.csv
│   │   ├── features.csv
│   │   └── stores.csv
│   └── processed
│       └── predictions.csv
│
├── notebooks
│   └── EDA.ipynb
│
├── src
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   ├── train_model.py
│   ├── predict.py
│
├── dashboard
│   └── retail_dashboard.pbix
│
├── main.py
├── requirements.txt
└── README.md
```

---

# Exploratory Data Analysis

Exploratory analysis was conducted to understand sales patterns and identify key drivers of demand.

Key analyses performed:

* Weekly sales trends over time
* Sales distribution by store
* Holiday impact on sales
* Seasonal sales patterns

Insights discovered:

* Sales increase significantly during holiday periods
* Larger stores generate higher revenue
* Economic indicators such as unemployment slightly impact sales demand
* Sales exhibit strong seasonal patterns

---

# Feature Engineering

To improve forecasting accuracy, several time-series features were created:

Lag Features
Previous week sales (lag_1)
Two weeks previous sales (lag_2)

Rolling Features
4-week rolling average sales

Date Features
Month
Week number
Year

These features help the machine learning model capture **temporal patterns and seasonality**.

---

# Machine Learning Model

Model used: **XGBoost Regressor**

Reason for selection:

* Strong performance on tabular datasets
* Handles nonlinear relationships effectively
* Widely used in real-world forecasting problems

Training pipeline includes:

1. Feature engineering
2. Train-test split based on time series
3. Model training
4. Forecast prediction
5. Model evaluation

---

# Model Evaluation

Evaluation metric used:

Root Mean Squared Error (RMSE)

RMSE measures the average difference between **actual sales and predicted sales**.

Lower RMSE indicates better model performance.

---

# Power BI Dashboard

A business intelligence dashboard was created to visualize insights and predictions.

Dashboard includes:

### Sales Overview

Total Sales KPI
Sales trend over time
Sales by store
Monthly sales distribution

### Demand Forecasting

Actual vs predicted sales
Forecast comparison across stores

### Inventory Optimization

Recommended reorder quantity
Demand forecast insights

The dashboard helps business stakeholders **make data-driven inventory decisions**.

---

# Example Use Case

A retail company can use this system to:

* Predict next week's product demand
* Identify high-performing stores
* Adjust inventory levels proactively
* Reduce overstocking and stockouts

---

# Future Improvements

Possible enhancements include:

* Deep learning forecasting using LSTM
* Automated data pipelines using Airflow
* Real-time prediction API using FastAPI
* Cloud deployment using AWS or Azure
* Integration with Snowflake or BigQuery

---

# Author

Manas Jadhav
Data Analyst | Power BI Developer | Data Engineering Enthusiast

LinkedIn
GitHub

---

# License

This project is developed for **educational and portfolio purposes**.
