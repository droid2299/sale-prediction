# Grocery Sale Time Predictions using Time Series Analysis
Our application analyzes monthly costs of food and other miscellaneous goods, and predicts the price of each item in the following month. It utilizes food price data from the Government of Canada, dating back from 1991, and trains it using a SARIMA (Seasonal Autoregressive Integrated Moving Average) model to predict the price in the next month.

# Installation
```
!pip install -r requirements.txt
```

# Description
## Dataset:

The dataset we used is titled ["Monthly average retail prices for food and other selected products"](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1810000201) by the Government of Canada. It has prices of various groceries from 1991 to 2022.

# How to Run:
The ```time_series_analysis_data_exploration.ipynb``` file is the notbook in which we did a through data exploration of the dataset. We concluded that using only `Log Transform ` would be helpful for our model.

In the `time_series_analysis_grid_serach.ipynb` file, we did a grid search for the SARIMA model for each of the product in our dataset and saved the weights to a `pickle file`. This was done using multithreading so that we could save time and train multiple SARIMA models at once. We also have the option of running the training without grid search by passing the parameters we seem fit for the model. Do not forget to update the path to save the weights and load the dataset.

In the `time_series_analysis_inference.ipynb` file, we do the forcasting. We firstly load the weights and take in the product name and run an inference to find forecast. Do not forget to change the path to the weghts files.


