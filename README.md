# Forecasting-Analysis

This project aims to forecast the real exchange rate between the United States (home country) and Japan (foreign country) using ARIMA models. The analysis was conducted using Python, with data sourced from trusted platforms such as FRED and BIS for nominal exchange rates and CPI data. Six ARIMA models were implemented to evaluate the best fit for predicting future trends in the exchange rates.

**1. Dataset:**
Home Country: United States
Foreign Country: Japan
Variables: Nominal exchange rate, CPI for both countries, and real exchange rate
Data Period: Monthly from February 2010 to January 2024
Data Sources: Federal Reserve Economic Data (FRED) for exchange rates, and BIS for Consumer Price Index (CPI)

**2. Data Preprocessing:**
Log Transformation: Applied to stabilize variance and linearize relationships between variables.
Stationarity Check: Augmented Dickey-Fuller (ADF) tests were applied to verify stationarity, crucial for time series forecasting. Non-stationary variables were differenced to achieve stationarity.
First-order Differencing: Successful for nominal exchange rates and CPI for the US, but CPI for Japan required second-order differencing.

**3. Models Implemented:**
Six ARIMA models were tested using different combinations of autoregressive (AR), moving average (MA), and differencing (I) terms:

ARIMA (101): Moderate accuracy
ARIMA (100): Showed slightly less autocorrelation in residuals
ARIMA (001): Similar trend to the others
ARIMA (111): Explored differencing, but did not show significant improvement
ARIMA (110): Moderate fit with some autocorrelation in residuals
ARIMA (011): Best model with the lowest AIC and BIC values and no significant autocorrelation

**4. Forecasting:**
Final Model: ARIMA (011) was selected as the best-performing model for forecasting future real exchange rates. This model had the lowest AIC and BIC values and passed residual diagnostic tests like the Ljung-Box statistic.
Results: Forecasts showed a steady increase in the real exchange rate for the upcoming year, with minor fluctuations in monthly predictions.

**5.Methodology:**

Box-Jenkins Approach: Identified and fitted ARIMA models, followed by diagnostic checks and forecast generation.
Residual Analysis: Performed to ensure no significant autocorrelation remained, confirming the models captured underlying trends.
Statistical Testing: Conducted for Purchasing Power Parity (PPP) using ADF and Engle-Granger cointegration tests, verifying the relationship between inflation and exchange rates.


**Conclusion:**
The ARIMA (011) model proved to be the most efficient in forecasting real exchange rates between the US and Japan. The repository includes all scripts and documentation, making it suitable for replicating the analysis with different datasets or extending the forecast for future periods.
