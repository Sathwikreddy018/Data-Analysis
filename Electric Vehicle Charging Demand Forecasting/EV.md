# Electric Vehicle Charging Demand Forecasting

This project leverages time series forecasting to predict the demand for electric vehicle (EV) charging stations in Palo Alto, CA, using historical charging data, weather data, and traffic events. The goal is to optimize EV infrastructure by accurately forecasting charging demand and recommending strategies for station placement, capacity, and operations.

---

## Project Overview

- **Objective**: Forecast EV charging demand to aid in infrastructure optimization and operational improvements.
- **Methodology**: Time series analysis using Prophet with external regressors (weather, traffic).
- **Data**: 
  - **EV Charging Data** (2018-2020) from Palo Alto charging stations (~100,000 records).
  - **Weather Data** (hourly measurements) from Meteostat (temperature, humidity, precipitation, etc.).
  - **Traffic Data** (116,000 events) including congestion, accidents, and road closures.

---

## Key Insights

- **Temporal Patterns**: Weekday charging peaks in the morning and evening; weekend peaks at midday. Summer months exhibit higher overall usage.
- **Weather Impact**: Temperature positively correlates with charging duration, while rain negatively impacts charging demand.
- **Traffic Impact**: Traffic congestion reduces charging station accessibility but increases session duration.

---

## Methodology

1. **Data Preprocessing**: Handle missing values, outliers, and time-based feature extraction.
2. **Feature Engineering**: Incorporate external regressors such as weather and traffic data.
3. **Time Series Decomposition**: Decompose the time series into trend, seasonality, and residual components.
4. **Modeling with Prophet**: Use Facebook's Prophet for time series forecasting with automatic handling of seasonality and holidays.
5. **Cross-Validation**: Time-based validation using expanding windows for real-world forecasting simulation.

---

## Forecast Results (kWh)

| Horizon     | Avg Prediction (kWh) | Avg CI Width (kWh) |
|-------------|----------------------|-------------------|
| Next Day    | 9.72                 | 11.32             |
| Next Week   | 9.77                 | 11.44             |
| Next Month  | 10.13                | 12.38             |
| 3 Months    | 10.69                | 13.28             |
| 6 Months    | 11.16                | 14.12             |
| 1 Year      | 11.65                | 15.00             |

---

## Charging Optimization Strategy

- **Capacity Optimization**: Add charging ports at stations with >80% occupancy during peak hours.
- **Location Strategy**: Focus on areas with high traffic but low charging availability.
- **Charging Speed Mix**: Install fast (DC) chargers where session durations are shorter, and standard chargers (Level 2) where users tend to stay longer.
- **Dynamic Pricing**: Implement time-variable pricing to balance demand and encourage charging during off-peak hours.
- **Predictive Maintenance**: Schedule maintenance during predicted low-usage periods.
- **User Communication**: Provide real-time availability forecasts to users.
- **Grid Coordination**: Collaborate with utilities to manage charging loads during high-demand periods.

---

## Requirements

- Python 3.x
- Libraries: `pandas`, `numpy`, `prophet`, `matplotlib`, `seaborn`, `scikit-learn`, `meteostat`, `statsmodels`

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ev-charging-demand-forecast.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebooks or Python scripts to reproduce the analysis and model training.

---

## Acknowledgements

- **Prophet**: Facebook's forecasting tool.
- **Meteostat**: For weather data.
- **Palo Alto City**: For providing charging station data.

---
