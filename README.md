# Electricity Demand Prediction with SARIMA Models

This repository contains the code and documentation for predicting electricity demand in different buildings using Seasonal Autoregressive Integrated Moving Average (SARIMA) models. The dataset used for this project is provided by the [Building Data Genome Project 2](https://github.com/buds-lab/building-data-genome-project-2).

## Introduction

This project is part of a seminar on Machine Learning in Renewable Energy Systems, from the research group [Machine Learning in Sustainable Energy Systems](https://www.mlsustainableenergy.com/) at the University of Tübingen. The goal of this seminar is to explore the application of machine learning techniques to address challenges in renewable energy systems. In the coding track of this seminar and in this particular project, we focus on predicting electricity demand in various buildings, a crucial aspect of energy management and optimization.

## Dataset

The dataset used in this project is provided by the [Building Data Genome Project 2](https://github.com/buds-lab/building-data-genome-project-2). It contains valuable information about various buildings, including historical electricity consumption data, weather data, and building characteristics.

## Methodology

In this project, I used Seasonal Autoregressive Integrated Moving Average (SARIMA) models to predict electricity demand for each building individually. SARIMA models are suitable for time series forecasting tasks and can capture both trend and seasonality in the data. I did a preliminary analysis 

## Project Structure

The project is organized as follows:

- `data/`: This directory contains the dataset from the [Building Data Genome Project 2](https://github.com/buds-lab/building-data-genome-project-2)

- `models/`: This directory contains the pickled sarima models for each of the buildings used to gnerate the results


- `results/`: In this directory obtained results from the predictions can be found. It contains errors and predictions.

- `results/errors/`: This directory contains pickled files of the errors for the different predictions horizons of the predicted buildings.

- `results/predictions/`: This directory contains pickled files of the predictions of one week made by the SARIMA models.
- 

## Usage

To replicate the results or use the SARIMA models for your own predictions, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/mdeppner/electricity_demand_prediction_arima.git
   ```

2. Navigate to the project directory:

   ```bash
   cd electricity_demand_prediction_arima
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Unzip models in the folder `models/`
    There have been models that were too large to push on github (> 2 GB)
    To fully execute the notebook these models in 'zip_one_sarima_model_order_1_0_1_seasonal_order_2_0_2_24.zip' and 'zip_two_sarima_model_order_1_0_1_seasonal_order_2_0_2_24.zip' need to be unzipped in the models folder. Please make sure there is no extra order created in the models order, unzip them directly in place.

5. Explore the Jupyter notebook and execute 
    This notebook is designed to be run completely once all the requirements and imports are done and the models are unzipped

## Results

The prediction results and evaluation metrics can be found in the `results/` directory. These results demonstrate the accuracy and performance of the SARIMA models in predicting electricity demand for different buildings and are also visualized and discussed in the jupyter notbeook.

## Notes

This is the second approach of this project. My initial approach to this project was to predict electricity consumption using Gaussian Processes. I identified the time series in the dataset that showed the highest correlations with the timeseries to be predicted and based on these time series and the Gaussian Process Regression model I predicted the electricity demand. However, the implementation of this approach had some bugs which were beyond the scope of this seminar to make this experiment executable. Here is the link to the repository of the first approach, which has not been further developed since the first deadline and is not in a final state [github.com/mdeppner/energy_demand_prediction_for_buildings](https://github.com/mdeppner/energy_demand_prediction_for_buildings)

 After the emerging problems, I decided to use a new approach with ARIMA models for prediction, which can be found in this repository