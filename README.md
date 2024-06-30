# Forecasting Model - Machine Learning for Time Series

The core challenge of this project lies in the need to understand and predict energy consumption and production in Turkey over several years, using a detailed dataset comprising hourly data. This task is essential to ensure the stability and efficiency of the country's power grid, as well as to effectively plan energy supply and future investments in the energy sector. The complexity of the Turkish energy landscape, characterized by a diversity of energy production sources and demand variations influenced by multiple and variable factors, poses a significant challenge. Therefore, the challenge is to accurately and efficiently analyze and model these complex data to provide reliable and actionable forecasts for policymakers, grid operators, and energy market participants. 

The provided dataset offers a detailed insight into Turkey's energy landscape between 2018 and 2023, presenting crucial information on energy consumption and production, as well as associated prices. With hourly data, it allows for granular analysis of trends and variations in electricity demand and generation throughout the period considered. The amount of energy consumed, measured in megawatt-hours (MWh) per hour, is a fundamental indicator for assessing the nation's energy needs.

To address the challenge of forecasting energy consumption and production in Turkey, we developed five distinct models, each bringing a unique approach to short-term forecasting. First, we used the naive model as a benchmark, providing a baseline for evaluating the performance of other models. Next, we explored two univariate analysis approaches, namely ARIMA and Prophet, which focus on modeling trends and patterns in energy consumption and production data without considering other variables.

Concurrently, we also implemented two multivariate analysis approaches, LGBM and LSTM, which took into account interactions between different variables to improve forecast accuracy. These models were particularly effective in capturing the complex relationships between different energy production sources, electricity prices, and other factors influencing energy demand.

Our primary goal was to achieve short-term forecasts, specifically focusing on predicting the 6th hour based on data from the previous 5 hours. This approach enables increased responsiveness to rapid fluctuations in energy demand and production, which is crucial for ensuring grid stability and meeting real-time needs. By combining these different approaches, we were able to evaluate the relative performance of each model and identify the most effective methods for short-term forecasting in the Turkish energy context. This, in turn, helped develop valuable tools and techniques for efficient grid management and energy planning in the country.

# 

![Results : ](/Users/maysaslimani/Desktop/Capture d’écran 2024-06-30 à 10.00.33.png)

Basic models, Seasonal naive and Naive mean 24 hours, showed relatively poor performance with high MAE and RMSE and negative R2 values, indicating that these models are not adequate for capturing the complexity of the data. These simplistic approaches can serve as baselines for comparison, but they are generally not sufficient for accurate predictions as they do not account for trends, seasonality, or other factors influencing the time series.

The ARMA model, a classical method in time series analysis, slightly improved performance compared to naive models but still has a negative R2, indicating it does not fit well to non-stationary data or series with complex dynamics.

Prophet is a robust model for data with nonlinear trends and strong seasonality, and its best R2 score among the initial methods shows its ability to model the time series more effectively. With much lower MAE and RMSE than the previous models, Prophet proves to be a solid choice for energy consumption data that may exhibit distinct seasonal patterns and influential holiday events.

LSTM and LightGBM models offer exceptional performance, with R2 values approaching perfection and the lowest MAE and RMSE errors. This indicates an excellent ability to accurately predict energy consumption while capturing the underlying complexity of the time series. LSTMs are particularly suited for learning from sequences of data due to their internal memory, allowing them to capture long-term dependencies in the data. LightGBM, on the other hand, uses efficient gradient boosting and can handle large-dimensional datasets, which is often the case with multivariate time series.
