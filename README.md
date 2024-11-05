# SARIMAX_FORECASTING_GRID_SEARCH
In this project, we will apply one of the most widely used algorithms in time series analysis, SARIMAX, in Python. We will configure a grid search to find the optimal parameters and present the results of the best SARIMAX model.

## About the Data
The data was extracted from a Chilean open-source website (https://datos.gob.cl/dataset/registro-de-importacion-2024). The data is uploaded to the site monthly, so the process involved extracting each month’s total imports to Chile from 2018 to the present. This resulted in a database with more than 20 million rows and over 200 attributes. For this project, we filtered records where [NOMBRE_TIPO_CARGA] == "GRANEL SÓLIDO", representing breakbulk import goods, and selected 33 of the 200+ available attributes relevant to this analysis
