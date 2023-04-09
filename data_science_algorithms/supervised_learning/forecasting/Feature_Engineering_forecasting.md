## Time Series Forecasting

## Feature Types
1. Lag Features
2. Features with known values in the future - Ad spend
3. Features with unknown value in the future - weather
4. Static Features - like country


## Multi-Step forecasting
 - Direct forecasting
   - Same input data - multiple target variables
   - Need to maintain multiple models
 - Recursive forecasting
   - Use one model only
   - Forecast one step at a time 
   - use the forecast as the input for next forecast


## Properties
- Cross validation - data need to be split by time
- Creating Feature & target - Features built from target created on demand at predict time for test set
- Need trained model as well as training set at predict time
- Feature Engineering - Time series specific features & check for data leakage issues


## Feature Engineering
 - Imputation 
   - Forward fill, Backfill
   - Interpolate
 - Outliers
   - Identify
   - Dummy Variable
 - Transformation
   - Log
   - Box Cox
   - Seasonal & Trend adjustment
 - Encoding
   - One hot
   - Target mean, integer
 - Temporal
   - Calendar - day, week, month
   - Holidays
   - Cyclical Feature encoding
 - Past Features
   - Lag Features
   - Window Features
 - Trend & Seasonality
   - Time Variables
   - Change points
   - Step Changes
   - Fourier Series
   - Seasonal dummies
   - Seasonal lags


## Libraries
- Feature Engineering & pre-processing
  - tsfresh
    - Large number of time series features
    - Supports ML forecasting workflows
    - Multiple time series
  - Feature-engine
    - Create time series features on top of pandas
  - Darts 
    - Recursive Strategy
    - Some helper functions to create features
    - Multiple time series
    - Exogenous features
    - Time series cross-val
  - SKTIME
    - direct, recursive & multi-output strategy
    - Lots of transformers for feature engineering
    - Multiple time series
    - Exogenous features
    - Time Series cross val