# NIFTY 50 Stock Price Forecasting using ARIMA

## Project Overview

This project focuses on forecasting NIFTY 50 stock prices using the AutoRegressive Integrated Moving Average (ARIMA) time series model.

Historical NIFTY 50 daily price data is used to build the ARIMA forecasting model. The model automatically identifies an appropriate ARIMA configuration and generates forecasts for the next 90 trading periods.

The forecasted values are then compared with the actual market prices to evaluate the predictive performance of the model.

---

## Project Objective

The main objective of this project is to:

- Apply the ARIMA model to NIFTY 50 historical price data.
- Forecast future stock prices.
- Compare predicted values with actual market values.
- Evaluate the forecasting performance using statistical error metrics.

---

## Dataset

This project uses two datasets:

### 1. Historical Dataset

**Nifty 50 Historical Data (2014-2024) Daily.csv**

This dataset contains historical daily NIFTY 50 market data from 2014 to 2024 and is used for training the ARIMA model.

### 2. Future Dataset

**Nifty 50 Historical Data (2024-25).csv**

This dataset contains future observations used to compare the forecasted values with the actual market values.

The main variables include:

- Date
- Price
- High
- Low

The `Price` variable is used as the time series for ARIMA modeling.

---

## Methodology

The project follows the following workflow:

```text
Historical Data
      ↓
Data Cleaning and Preparation
      ↓
Time Series Creation
      ↓
Automatic ARIMA Model Selection
      ↓
Model Training
      ↓
90-Day Forecast
      ↓
Load Actual Future Data
      ↓
Actual vs Predicted Comparison
      ↓
Performance Evaluation
```

---

## Data Preparation

The following preprocessing steps are performed:

- Conversion of price columns from string to numeric format.
- Removal of commas from price values.
- Conversion of the `Date` column into datetime format.
- Sorting the dataset chronologically.
- Setting the `Date` column as the time series index.

---

## ARIMA Model

The ARIMA model is used for time series forecasting.

The model parameters are automatically selected using `auto_arima()` from the `pmdarima` library.

The model selection process is configured with:

- Non-seasonal ARIMA
- Stepwise search for efficient parameter selection
- Automatic selection of the ARIMA order

The selected model is then used to generate forecasts for the next 90 periods.

---

## Forecasting and Evaluation

The generated 90-day forecasts are compared with the corresponding actual NIFTY 50 prices.

The performance of the ARIMA model is evaluated using:

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted values.

### Root Mean Squared Error (RMSE)

Measures the magnitude of prediction errors in the original scale of the data.

### Mean Absolute Percentage Error (MAPE)

Measures the average percentage difference between actual and predicted values.

---

## Technologies and Libraries Used

This project was implemented using Python.

Main libraries include:

```python
pandas
numpy
pmdarima
scikit-learn
```

---

## Repository Structure

```text
NIFTY50-ARIMA-Forecasting/
│
├── Nifty 50 Historical Data (2014-2024) Daily.csv
├── Nifty 50 Historical Data (2024-25).csv
│
├── NIFTY50_ARIMA.ipynb
│
└── README.md
```

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Install the required libraries

```bash
pip install pandas numpy pmdarima scikit-learn
```

### 3. Open the notebook

Open:

```text
NIFTY50_ARIMA.ipynb
```

The notebook can be executed using:

- Jupyter Notebook
- JupyterLab
- Google Colab

### 4. Run all cells

Execute the notebook cells sequentially to:

1. Load the historical dataset.
2. Prepare the time series.
3. Automatically select the ARIMA model.
4. Generate a 90-day forecast.
5. Compare predicted values with actual values.
6. Calculate MSE, RMSE, and MAPE.

---

## Key Outputs

The project provides:

- Selected ARIMA model order.
- 90-day NIFTY 50 price forecasts.
- Actual vs predicted price comparison.
- Mean Squared Error (MSE).
- Root Mean Squared Error (RMSE).
- Mean Absolute Percentage Error (MAPE).

---

## Future Work

This project forms the forecasting stage following the Exploratory Data Analysis (EDA) of NIFTY 50 data.

Possible future extensions include:

- ARIMA model diagnostics.
- Visualization of actual vs predicted values.
- Residual analysis.
- Comparison with other forecasting models.
- Neutrosophic ARIMA (N-ARIMA).
- TNN-based forecasting.
- Comparative evaluation of all forecasting models.

---

## Author

**Drishti Agarwal**

M.Sc. Mathematics  
GLA University, Mathura

---

## Project Summary

This project demonstrates the application of the ARIMA time series model for forecasting NIFTY 50 stock prices. Historical market data is used to build the model, generate 90-day forecasts, and evaluate prediction accuracy by comparing the forecasts with actual market values using MSE, RMSE, and MAPE.
