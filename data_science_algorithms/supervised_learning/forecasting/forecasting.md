# Forecasting Techniques

### Traditional Methods

- Autoregression (AR)
- Moving Average (MA)
- Autoregressive Moving Average (ARMA)
- Autoregressive Integrated Moving Average (ARIMA)
- Seasonal Autoregressive Integrated Moving Average (SARIMA)
- Seasonal Autoregressive Integrated Moving Average with Exogenous Regressors (SARIMAX)
- Vector Autoregression (VAR)
- Vector Autoregression Moving Average (VARMA)
- Vector Autoregression Moving-Average with Exogenous Regressors (VARMAX)
- Simple Exponential Smoothing (SES)
- Holt Winter's Exponential Smoothing (HWES)

- NPTS (Non parametric Time series)
  - Standard NPTS
  - Seasonal NPTS
  - Climatological Forecaster
  - Seasonal Climatological Forecaster


### Neural Network Methods
- CNN-QR (convolutional Neural networ - quantile regression) 
- DeepAR+ 
- Prophet 
  - Additive model where non-linear trends are fit with yearly, weekly and daily seasonality
  - Strong seasonal effects and several seasons of historical data

### Other methods
- Approximating quantile function

## Evaluation Metrics
- Root mean square Error (RMSE)
- Weighted Quantile loss (wQL)
- Average weighted quantile loss (Average wQL)
- Mean absolute scaled error (MASE)
- Mean absolute percentage error (MAPE)
- Weighted absolute percentage error (WAPE)

## Forecast Type
- Mean forecast type
- Quantile forecast type - forecast at specified quantile


## Things to consider
- Forecast frequency
  - Minutes, hourly, daily, weekly, monthly
- Holiday events
- Change points
- Weather Index
- Geolocation data
- Hierarchy Levels
  - Bottom Up
  - Top Down
  - Middle out 
  - Optimal Reconciliation method (Scikit - hts)

## Forecast Explainability
- 

## Prediction Monitoring


## What-if Analysis


## Reference Links
- [Traditional Forecasting Models](https://machinelearningmastery.com/time-series-forecasting-methods-in-python-cheat-sheet/)
- [Seasonality Fourier Transform](https://blog.ah.technology/time-series-as-a-signal-fast-fourier-transform-to-decompose-seasonality-6810d2811feb)
- 


## Concepts

### Seasonality
 - Fast Fourier Transform
   - Amplitude
   - Period
   - Frequency
   - 