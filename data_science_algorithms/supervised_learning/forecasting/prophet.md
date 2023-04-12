# Prophet Model

- Prophet is a time series forecasting model developed by Facebook 
- that uses an additive model to predict future values 
- based on historical trends, seasonal patterns, and other relevant factors.

The model decomposes the time series into three main components:
 - trend - The trend component captures the overall direction of the time series over time,
 - seasonality - the seasonality component captures any recurring patterns or cycles that occur within the data.
 - and holidays - the holiday component accounts for the impact of one-time events that may affect the time series, such as major holidays or other important events.
 

- Prophet fits a model to historical data by analyzing these components and estimating the parameters that best capture the patterns and trends in the data. 
- It then uses these parameters to make future predictions.

To make a forecast, 
- Prophet first generates a range of possible values for each component of the time series.
- It then combines these components to create a range of possible future values for the time series as a whole. 
- The model also generates uncertainty intervals for each prediction, providing a measure of the confidence in the forecast.

Overall, Prophet is a flexible and powerful tool for time series forecasting, with many options for customizing the model to fit different types of data and forecasting needs.


## Customization in prophet model

Prophet is a highly customizable time series forecasting model that allows users to adjust many different aspects of the model to fit their specific data and forecasting needs. 
Here are some of the ways you can customize Prophet:

- Trend specification: 
  - You can choose from a variety of options for modeling the trend component of the time series, such as linear, logistic, or piecewise linear trends.

- Seasonality specification: 
  - You can customize the seasonality component by adjusting the number of Fourier terms used to model the seasonal patterns, or by specifying custom seasonalities.

- Holidays: 
  - You can include holidays that are relevant to the time series being forecasted, such as national holidays or major events, and adjust the way the model handles these holidays.

- Changepoints: 
  - You can specify the number and location of changepoints in the time series, which are points in time where the underlying trend or seasonality changes.

- Prior specification: 
  - You can adjust the strength of the priors used in the model to make it more or less flexible, depending on the amount of data available and the level of uncertainty in the forecasts.

- Modeling outliers: 
  - You can customize how the model handles outliers, such as by excluding them from the analysis or by modeling them explicitly.

- Additional regressors: 
  - You can include additional covariates that may be relevant to the time series being forecasted, such as economic indicators or weather data.

By customizing these different aspects of the Prophet model, users can tailor the forecasting approach to their specific data and gain more accurate and actionable insights from their forecasts.


## Fourier Terms for seasonality

- Fourier terms are a way to model periodic patterns in time series data using a series of sine and cosine waves. 
- In the context of Prophet, Fourier terms are used to model the seasonality component of the time series.

- The basic idea behind Fourier terms is that any periodic function can be represented as a sum of sine and cosine waves with different frequencies and amplitudes. 
- The number of Fourier terms used to model the seasonality component determines the level of detail in the seasonal patterns that the model can capture.

- In Prophet, the seasonality component is modeled using a set of Fourier terms with a user-specified number of harmonics. 
- Each harmonic includes two terms (one sine wave and one cosine wave) and is defined by a frequency (measured in cycles per year) and an amplitude.
- The model fits the amplitudes and frequencies of these harmonics to the seasonal patterns in the data, allowing it to capture both simple and complex seasonal patterns.

- By adjusting the number of Fourier terms used to model seasonality, 
- users can control the level of complexity of the seasonal patterns that the model can capture.
- More Fourier terms can capture more detailed seasonal patterns, but can also lead to overfitting if the number of terms is too high. 
- Conversely, fewer Fourier terms can lead to underfitting and a loss of important seasonal patterns in the data.


## Exogenour Variable

- Exogenous variables, also known as covariates or regressors, are external variables that may influence the time series being forecasted. 
- These variables are not part of the time series itself, but are instead included in the forecasting model as additional inputs to help improve the accuracy of the forecast.


- Exogenous variables can be any relevant external data that may impact the time series being forecasted, such as economic indicators, weather data, or other external factors that may affect the outcome being predicted. 
- Including exogenous variables in the forecasting model can help account for external factors that may not be captured by the time series alone, improving the accuracy of the forecast.


- In Prophet, exogenous variables can be included in the forecasting model by adding them to the input dataframe alongside the time series data. 
- The model then fits a regression model that takes into account the relationship between the exogenous variables and the time series being forecasted.


- Exogenous variables can be particularly useful in situations where the time series being forecasted is affected by external factors that are not captured by the time series data alone. 
- By including relevant external data in the forecasting model, users can generate more accurate and reliable forecasts that take into account a broader range of factors that may impact the outcome being predicted.
