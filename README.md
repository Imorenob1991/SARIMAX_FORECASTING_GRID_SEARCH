# SARIMAX_FORECASTING_GRID_SEARCH
In this project, we will apply one of the most widely used algorithms in time series analysis, SARIMAX, in Python. We will configure a grid search to find the optimal parameters and present the results of the best SARIMAX model.

## About the Data
The data was extracted from a Chilean open-source website (https://datos.gob.cl/dataset/registro-de-importacion-2024). The data is uploaded to the site monthly, so the process involved extracting each month’s total imports to Chile from 2018 to the present. This resulted in a database with more than 20 million rows and over 200 attributes. For this project, we filtered records where [NOMBRE_TIPO_CARGA] == "GRANEL SÓLIDO", representing breakbulk import goods, and selected 33 of the 200+ available attributes relevant to this analysis

## Methodology of the project
  - Data Wrangling: Reading the CSV file and preparing the data for time series analysis (with "Date" set as the index). Grouping data into a monthly series and generating general plots to identify key insights.
  - Decomposing the Time Series: We then decompose the series into trend, seasonality, and remainder. Through plots and measuring the strength, we identify the representation of the trend and seasonality in the time series.
- We then plot the ACF and PACF to identify if the moving average and autoregressive components of the models have significant lags or gradually tail off.
- Basic Time Series Modeling Using ARIMA: We apply the Moving Average Model (1,0,0), Autoregressive Model (1,0,1), and ARIMA (1,1,1).
- Plotting Results: We compare the fitted values with the actual observations and plot a 12-month forecast to assess the model's predictive accuracy.
- Grid Search for Optimal SARIMAX Parameters: We conduct a grid search to identify the optimal parameters (p, d, q) and (P, D, Q, S) that minimize AIC and provide the best model.
- Modeling, Fitting, and Forecasting with the Best SARIMAX: We fit and predict with the optimal SARIMAX model, plotting results to compare with the initial ARIMA models and observe any improvements.

  ## Results

  Initial Best ARIMA MODEL: AIC 1136

  ![ARIMA_PLOT](https://github.com/user-attachments/assets/b94be43b-d921-4ccc-8a11-c0a0490c2617)

  Comments: The model struggles to forecast accurately due to limitations in incorporating seasonal patterns.

  FINAL SARIMAX MODEL W/GRID SEARCH: AIC 988

  ![SARIMAX_PLOT](https://github.com/user-attachments/assets/bdfc734c-4a33-4cd1-b30c-5a6d995fe9c5)


  Comments: It's important to note that the model improved in terms of AIC (indicating a model with potentially better predictive capability). However, this does not mean that the  error values of the fitted model improved—in fact, they actually increased



  
