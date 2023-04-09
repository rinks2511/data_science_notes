

## Task for Time series analysis

- Visualization & EDA
  - Understanding temporal behaviour of data : seasonality, stationarity
  - Identifying underlying distribution and nature of temporal process producing data
- Estimation of past, present & future sales
  - filtering vs forecasting
- Classification of Time series
- Anomaly Detection of outlier points within time series


## Time Series v/s Cross Sectional data

- More opportunities for missing data points
- High degree of correlation between data points
- Time stamps or other measures of distance travelled along the temporal axis
  - Time zones, frequency irregularities


## Characteristics of Time series

- Data is collected sequentially
- Structure is characterized across data points
  - Seasonality & Cyles
  - Autocorrelation
  - Trends
- Stochastic behavior even as to behavioral regime
  - Change points
  - Regime shifts v/s drifts
  - gradual change

## Concerns for time series data
- Correlated errors (Time aware diagnostic required)
- Cross-validation
- Lookahead forecasting
- Stationarity


## State space models

- Box Jenkins ARIMA modeling
  - Excellent performance on small data set
  - Usually a baseline model
  - Problems with ARIMA
    - Not especially intuitive
    - No way to build in our underlying understanding how it works
      - Random walk element
      - Cyclical element
      - External regressors
    - Some system cycle more slowly or stochastically than can be easily described by ARIMA


# Structural Time series model
- Can be expressed in ARIMA form
- Fit via maximum likelihood/ Kalman filter
- Largely developed in econometrics
- Offer insight into Bayesian structure
- Posible to inject Bayesian analysis via priors on parameters


# State space models
- Filtering : distribution of current state at time t given all previous measurements up to and including time t
- Prediction : distribution of future state at time t + k, given all previous measuresment up to and including time t
- Smoothing : distribution of given state at time k given all previous and future measurement from 0 to T (last time)



