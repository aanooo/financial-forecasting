**Overview**
This project demonstrates how machine learning and time-series analysis can be applied to financial forecasting. Using quarterly financial data, it builds models to predict future revenue, detect anomalies in past performance, provide explainable insights into model predictions, and perform scenario-based what-if analysis to support financial planning.

**Data**

Source: Yahoo Finance  via the yfinance  Python API

Fallback: If Yahoo data isn’t available, the project generates synthetic financial data (with trends, seasonality, and random shocks) to ensure reproducibility

**Methods & Workflow: **

1. Data Collection & Cleaning:  
Fetch quarterly revenue and operating expense (OPEX)
Generate features: lags, rolling averages, growth rates

2. Forecasting Models
Linear Regression
Random Forest Regressor
XGBoost Regressor
ARIMA (time-series baseline)

3.Model Evaluation
Metrics: MAE, RMSE, MAPE
Visual comparisons of Actual vs Predicted revenue

4. Anomaly Detection
Isolation Forest flags unusual quarters (e.g. sudden drops or spikes)

5. Explainability (XAI)
SHAP values show which features (e.g. past revenue, growth, OPEX) most influenced predictions
Includes both global importance and local (per-quarter) explanations

6. Scenario Analysis
Interactive sliders to test “What if” cases:
Revenue shock (e.g. -10%)
OPEX increase (e.g. +20%)
Recomputes forecasts under new assumptions

**Tools & Libraries**
pandas, numpy → data wrangling
scikit-learn → regression, Random Forest, anomaly detection
xgboost → gradient boosting regression
statsmodels → ARIMA forecasting
shap → explainable AI for model predictions
plotly, matplotlib → visualization
ipywidgets → interactive scenario sliders
yfinance → financial data collection

**Results**
Forecast accuracy benchmarked across ML and ARIMA models
Clear visualization of predictions vs actual revenue
Anomaly detection highlights risky or unusual quarters
SHAP plots make ML predictions interpretable for business users
Scenario analysis supports sensitivity planning

**Why It Matters**
Financial analysts spend much of their time forecasting, analyzing variances, and building scenarios. This project automates those workflows with modern data science tools, showing how ML can:
Improve forecast accuracy
Provide early warnings for anomalies
Make predictions transparent and explainable
Enhance decision-making with interactive scenario planning
