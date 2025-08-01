## **Telecom Customer Churn Analysis & Electric Vehicle Charging Demand Forecasting**

This repository contains two distinct but data-driven projects aimed at improving operational efficiency and customer retention strategies across different industries: telecom services and electric vehicle (EV) infrastructure.

## Projects Overview

### 1. Telecom Customer Churn Analysis

This project focuses on analyzing and predicting customer churn in telecom services. The goal is to identify at-risk customers and provide actionable insights to develop targeted retention strategies using machine learning and data analytics.

#### Key Insights:
- Identifying patterns in **customer value**, **subscription length**, and **usage behavior** to predict churn.
- Proposing strategies such as **complaint resolution enhancement** and **usage-based interventions** to reduce churn.

#### Technologies Used:
- **Machine Learning**: Random Forest, Decision Tree Classifications
- **Data Analysis**: pandas, numpy, matplotlib, seaborn
- **SQL Database** for data aggregation

#### Model Performance:
- **Random Forest**: Precision (97%), Recall (95%), F1-Score (96%)
- **Decision Tree**: Precision (94%), Recall (97%), F1-Score (96%)

---

### 2. Electric Vehicle Charging Demand Forecasting

This project uses time series forecasting to predict the demand for electric vehicle (EV) charging stations in Palo Alto, CA. It leverages historical charging data, weather conditions, and traffic events to recommend strategies for optimizing EV infrastructure.

#### Key Insights:
- Charging demand exhibits **temporal patterns** based on time of day and seasonality.
- Weather and **traffic congestion** influence charging duration and station accessibility.
- Forecasts inform strategies such as **capacity optimization**, **dynamic pricing**, and **station placement**.

#### Technologies Used:
- **Time Series Forecasting**: Prophet
- **Data Analysis**: pandas, numpy, matplotlib, seaborn
- **External Data**: Meteostat (weather), Traffic Data (events)

#### Forecasting Results (kWh):
- Next Day: **9.72 kWh**
- Next Month: **10.13 kWh**
- 1 Year: **11.65 kWh**

---

## Repository Structure

```bash
├── telecom-customer-churn-analysis/
│   ├── Churn.md
│   ├── Customer Churn.csv
│   ├── TeleChurnPred.ipynb
│   ├── Telecom Customer Churn Analysis.pptx
│   └── telecom churn.db
├── ev-charging-demand-forecasting/
│   ├── EV CHARGING TABLEAU DASHBOARD.docx
│   ├── EV.md
│   ├── EVCharging.twb
│   ├── EVForecast.twb
│   ├── EVforecast.ipynb
│   ├── Electric Vehicle Charging Demand Forecasting.pptx
│   ├── forecast 3months.csv
│   ├── forecast 6months.csv
│   ├── forecast_day.csv
│   ├── forecast_month.csv
│   ├── forecast_week.csv
│   └── forecast_year.csv
└── README.md

