
# Forecasting Process
In ecommerce, forecasting is performed to predict future demand for products or services, which helps in making decisions related to inventory management, production planning, pricing, and promotions. Here are some steps involved in performing forecasting on ecommerce:

- Data collection: 
  - The first step in performing forecasting is to collect historical data on sales, traffic, customer behavior, and other relevant metrics from various sources, such as transactional databases, web analytics tools, and social media platforms.

- Data preprocessing: 
  - The collected data may contain missing values, outliers, or noise that need to be handled before modeling. 
  - Preprocessing techniques such as imputation, filtering, and normalization can be applied to clean and transform the data.

- Time series modeling: 
  - Time series models, such as ARIMA, SARIMA, and Prophet, can be applied to model the underlying patterns and trends in the data and to make future predictions. 
  - These models can be trained on a subset of historical data and validated on a holdout set to evaluate their performance.

- Ensemble methods: 
  - Ensemble methods, such as bagging and boosting, can be used to improve the accuracy and stability of the forecasting models by combining multiple models or using them in sequence.

- Performance evaluation: 
  - The performance of the forecasting models can be evaluated using metrics such as MAE, MSE, RMSE, MAPE, and SMAPE, as discussed earlier. 
  - The models can also be compared with each other and with the performance of a baseline model to determine their effectiveness.

- Deployment and monitoring: 
  - Once the forecasting models are developed and evaluated, they can be deployed into production to make real-time predictions. 
  - It is important to monitor the performance of the models over time and to update them as new data becomes available or as the business needs change.

These are some common steps involved in performing forecasting on ecommerce. 
It is important to note that the specific techniques and methods used may vary depending on the nature of the data and the business goals.



## Time Series Components

The different components of a time series forecasting model can be classified into two categories: deterministic and stochastic.

- **Deterministic components:** These are the components that are predictable and can be modeled exactly. The deterministic components of a time series include:
    - **Trend:** 
      - A trend represents the long-term increase or decrease in the time series.
      - It can be modeled using a linear or nonlinear regression model.
    - **Seasonality:** 
      - Seasonality refers to the repeating pattern that occurs at fixed intervals of time, such as daily, weekly, or yearly.
      - It can be modeled using a seasonal decomposition model or by including dummy variables in a regression model.
    - **Calendar effects:** 
      - Calendar effects refer to events that occur on a specific date, such as holidays or weekends. 
      - These effects can be modeled using dummy variables in a regression model.

- **Stochastic components:** These are the components that are not predictable and are modeled using statistical methods. The stochastic components of a time series include:
  - **Error term:** 
    - The error term represents the random fluctuations or noise in the time series that cannot be explained by the deterministic components. 
    - It can be modeled using autoregressive integrated moving average (ARIMA) models or other similar models.
  - **Autocorrelation:** 
    - Autocorrelation refers to the correlation between the values of the time series at different points in time. 
    - It can be modeled using autoregressive (AR) models or moving average (MA) models.
  - **Seasonal variation:** 
    - Seasonal variation can also have a stochastic component, which can be modeled using seasonal ARIMA models or other similar models.



## Stationarity

### What is stationarity?
- Stationarity is an important concept in time series modeling.
- A stationary time series is one in which the statistical properties (such as the mean and variance) remain constant over time. 
- This means that the time series does not exhibit any trend, seasonal, or cyclical patterns, and the statistical properties of the series do not depend on the time at which the series is observed.

There are three types of stationarity that are commonly considered in time series modeling:

1 .Strict stationarity: 
- A time series is said to be strictly stationary if 
  - the joint distribution of any set of observations is the same as the joint distribution of the same set of observations shifted in time.

2. Weak stationarity: 
   - A time series is said to be weakly stationary 
   if the mean, variance, and autocovariance are constant over time.

3. Trend stationarity: 
- A time series is said to be trend stationary if 
 the mean and variance are constant over time but there is a trend present in the data.



### How to make a series stationary?
If a time series is not stationary, there are several techniques that can be used to make it stationary. Here are some common methods:

- Differencing:
  - Differencing is a technique where the difference between consecutive observations is taken. 
  - This can be done once or multiple times until the resulting series is stationary.

- Logarithmic transformation: 
  - Taking the logarithm of a series can help to stabilize the variance and make the series stationary.

- Seasonal adjustment: 
  - If a time series exhibits seasonal patterns, seasonal adjustment can be used to remove the seasonality and make the series stationary.

- Removing trends: 
  - If a time series exhibits a trend, the trend can be removed by fitting a regression model and subtracting the trend component from the series.

- Box-Cox transformation: 
  - The Box-Cox transformation is a technique that can be used to transform the data to achieve stationarity by raising the series to a power that varies based on the data.

- Combination of techniques: 
  - In some cases, a combination of these techniques may be required to achieve stationarity.

Once the series has been made stationary, it is important to check whether the statistical properties of the series are constant over time. 
This can be done by examining the autocorrelation function (ACF) and partial autocorrelation function (PACF) of the series. 
If the ACF and PACF indicate that the series is stationary, then it is suitable for use in time series modeling.


### How to check if the series is stationary or not?

There are several statistical tests that can be used to check whether a time series is stationary or not. Here are some common tests:

- Augmented Dickey-Fuller (ADF) test: 
    - The ADF test is a widely used test for stationarity.
    - It tests the null hypothesis that a unit root is present in the time series, which implies that the series is non-stationary. 
    - If the p-value obtained from the test is less than the significance level (e.g., 0.05), then the null hypothesis can be rejected, indicating that the series is stationary.

- Kwiatkowski-Phillips-Schmidt-Shin (KPSS) test:
  - The KPSS test is another commonly used test for stationarity.
  - It tests the null hypothesis that the series is stationary against the alternative hypothesis that the series has a unit root, indicating non-stationarity.
  - If the p-value obtained from the test is greater than the significance level, then the null hypothesis can be accepted, indicating that the series is stationary.

- Phillips-Perron (PP) test:
  - The PP test is similar to the ADF test, but it uses a different method for estimating the parameters of the test. 
  - It also tests for the presence of a unit root in the series.

- Visual inspection: 
  - Another way to check for stationarity is to visually inspect the time series plot.
  - If the plot shows a clear trend or seasonality, then the series is likely to be non-stationary.


# Forecasting Methods

There are several methods of time series forecasting, and the choice of method depends on the nature of the data and the forecasting goals. Here are some common methods:

- Simple Moving Average (SMA): 
  - SMA is a method that uses the average of a fixed number of past data points to forecast the future values. 
  - It is a simple and easy-to-implement method, but it may not be suitable for time series data with complex patterns.

- Exponential Smoothing (ES): 
  - ES is a method that assigns exponentially decreasing weights to past observations, with the most recent observations being weighted more heavily. 
  - There are several variations of the ES method, such as Simple Exponential Smoothing, Holt's Linear Exponential Smoothing, and Holt-Winters' Exponential Smoothing, which incorporate trend and seasonality components.

- Autoregressive Integrated Moving Average (ARIMA):
  - ARIMA is a method that models the autoregressive and moving average relationships in the time series. 
  - It involves identifying the order of differencing (to make the series stationary), the autoregressive order, and the moving average order, and fitting a model based on these parameters.

- Seasonal Autoregressive Integrated Moving Average (SARIMA):
  - SARIMA is a variation of ARIMA that includes a seasonal component, in addition to the autoregressive and moving average components. 
  - It is suitable for time series data with seasonal patterns.

- Prophet: 
  - Prophet is a forecasting method developed by Facebook that uses an additive model to decompose the time series into trend, seasonality, and holiday components. 
  - It also incorporates Bayesian modeling techniques and includes several customizable parameters.

- Deep Learning methods: 
  - Deep learning methods, such as Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models, have shown promise in time series forecasting, particularly for complex data with multiple seasonalities and irregular patterns.


## Forecasting Methods Evaluation Techniques
There are several methods to evaluate the accuracy and performance of a forecasting method. Here are some common evaluation techniques:

- Mean Absolute Error (MAE): 
    - MAE measures the average absolute difference between the actual and predicted values. 
    - Lower values of MAE indicate better performance.

- Mean Squared Error (MSE): 
  - MSE measures the average squared difference between the actual and predicted values. 
  - It gives more weight to larger errors than MAE. Lower values of MSE indicate better performance.

- Root Mean Squared Error (RMSE): 
  - RMSE is the square root of MSE and is used to compare the performance of different models. 
  - Lower values of RMSE indicate better performance.

- Mean Absolute Percentage Error (MAPE): 
  - MAPE measures the percentage difference between the actual and predicted values.
  - It is useful for comparing the performance of models across different scales of data.

- Symmetric Mean Absolute Percentage Error (SMAPE):
  - SMAPE is another percentage-based measure that is less sensitive to extreme values than MAPE.

- Theil's U-Statistic: 
  - Theil's U-Statistic measures the ratio of the root mean squared error of the model to the root mean squared error of a naive model that assumes the future value is equal to the most recent observed value. 
  - A value of less than 1 indicates better performance than the naive model.

- Forecast Value Added (FVA): 
  - FVA measures the value added by the forecasting process, taking into account the cost of errors and the cost of forecasting. 
  - It is useful for evaluating the economic impact of forecasting accuracy.

These evaluation techniques can be applied to both in-sample (training data) and out-of-sample (test data) data sets. It is important to evaluate the performance of a forecasting method on multiple metrics and to compare the results with the performance of other methods to choose the best method for the given data set and forecasting goals.


## Forecasting Data pre-processing steps

Data pre-processing is a critical step in forecasting as it helps to clean and transform the raw data into a format suitable for modeling. Here are some common data pre-processing steps in forecasting:

- **Data cleaning:** 
  - The first step in pre-processing is to identify and handle missing or erroneous data.
  - Missing data can be imputed using methods such as mean, median, or regression imputation. 
  - Erroneous data, such as outliers or noise, can be detected and removed using statistical or machine learning techniques.

- **Data transformation:** 
  - The raw data may not be in a suitable format for modeling. 
  - Data transformation techniques, such as normalization, scaling, or logarithmic transformation, can be applied to convert the data into a more appropriate format.

- **Seasonality adjustment:** 
  - Seasonality refers to the regular patterns that occur in the data over time, such as daily, weekly, or monthly cycles. 
  - Seasonality can be removed using techniques such as seasonal differencing or seasonal decomposition.

- **Trend removal:** 
  - Trends refer to the long-term patterns in the data, such as overall growth or decline. 
  - Trends can be removed using techniques such as detrending or differencing.

- **Feature engineering:** 
  - Feature engineering involves creating new features or variables from the existing data that may be relevant for modeling. 
  - For example, features such as day of the week, time of day, or weather data may be added to improve the forecasting accuracy.

- **Data splitting:**
  - The data is typically split into training and test sets to evaluate the performance of the forecasting models. The training set is used to fit the model, while the test set is used to evaluate the model's accuracy.

These are some common data pre-processing steps in forecasting. It is important to note that the specific steps and techniques used may vary depending on the nature of the data and the business goals.


## Hierarchiacal Forecasting

- Hierarchical forecasting is a technique used to forecast sales at multiple levels of a product hierarchy, such as SKU, product category, brand, or region. 
- The goal is to generate accurate forecasts at different levels of aggregation while maintaining consistency across the hierarchy.

Here are some common methods used for hierarchical sales forecasting:

- **Bottom-up forecasting**: 
  - This method involves forecasting the sales of individual SKUs or products first and then aggregating the forecasts to higher levels of the hierarchy.
  - This approach is useful when the demand for each product is independent and not influenced by other products in the hierarchy.

- **Top-down forecasting**: 
  - This method involves forecasting the sales of higher-level aggregates first, such as product categories or brands, and then disaggregating the forecasts to lower levels of the hierarchy. 
  - This approach is useful when the demand for lower-level products is driven by the demand for higher-level products.

- **Combination forecasting**: 
  - This method involves combining both bottom-up and top-down approaches to generate forecasts at different levels of the hierarchy. 
  - This approach is useful when the demand for some products is driven by higher-level aggregates, while the demand for other products is independent.

- **Forecast reconciliation**:
  - This method involves reconciling the forecasts generated at different levels of the hierarchy to ensure consistency and accuracy. 
  - This approach involves adjusting the forecasts at each level to ensure that they add up to the forecasts at higher levels of the hierarchy.

In practice, a combination of these methods may be used, depending on the nature of the data and the business goals. The specific methods used may also vary depending on the level of the hierarchy being forecasted and the availability of data at each level.



# Ecommerce Forecasting

E-commerce sites use a variety of techniques to perform forecasting to predict demand and sales for products. Here are some common methods used by e-commerce sites for forecasting:

- Time series analysis: 
 - This method involves analyzing historical data to identify patterns and trends in the data, such as seasonality, trends, and cyclical patterns. 
 - Time series models, such as ARIMA and exponential smoothing, are then used to forecast future sales.

- Machine learning: 
  - Machine learning algorithms, such as neural networks, random forests, and gradient boosting, can be used to analyze historical data and predict future sales. 
  - These algorithms are particularly useful when there are complex interactions between variables that influence demand.

- Customer segmentation: 
  - E-commerce sites may segment their customers based on demographics, purchasing behavior, or preferences. 
  - This information can be used to forecast demand and sales for different customer segments.

- Web analytics: 
  - E-commerce sites can analyze web traffic and user behavior to predict demand and sales. 
  - For example, site traffic and clickstream data can be used to forecast sales for specific products.

- External data sources: 
  - E-commerce sites may use external data sources, such as weather data, economic indicators, or social media trends, to forecast demand and sales.

- Collaborative filtering:
  - Collaborative filtering is a technique used to recommend products to customers based on their past behavior or preferences.
  - This information can be used to forecast demand and sales for specific products.

In practice, e-commerce sites may use a combination of these techniques to generate accurate forecasts.
The specific methods used may vary depending on the nature of the data and the business goals.



# Libraries 

Python has a rich ecosystem of libraries for time series forecasting. Some popular libraries for forecasting in Python include:

- Prophet: 
  - A time series forecasting library developed by Facebook that provides a simple and intuitive interface for fitting and forecasting time series data.

- ARIMA: 
  - A time series forecasting library in Python that implements the autoregressive integrated moving average (ARIMA) model, which is a popular and flexible method for modeling time series data.

- Statsmodels:
  - A Python library for statistical modeling that includes functionality for time series analysis and forecasting, including ARIMA and other models.

- TensorFlow: 
  - A popular deep learning library in Python that includes functionality for time series forecasting, such as the Long Short-Term Memory (LSTM) model.

- Scikit-learn: 
  - A Python machine learning library that includes a number of time series forecasting models, including the random forest and gradient boosting regressor models.

- Prophet Multi-Regression (pmr): 
  - An extension of Prophet to handle multiple regressors for forecasting.

- PyFlux:
  - A time series modeling and forecasting library in Python that includes functionality for Bayesian structural time series models, dynamic linear models, and more.

These are just a few examples of the many libraries available for time series forecasting in Python. The choice of library depends on the specific needs and requirements of the forecasting task at hand.