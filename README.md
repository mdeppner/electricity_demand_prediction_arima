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

4. Explore the Jupyter notebooks in the and execute the notebook 

## Results

The prediction results and evaluation metrics can be found in the `results/` directory. These results demonstrate the accuracy and performance of the SARIMA models in predicting electricity demand for different buildings and are also visualized and discussed in the jupyter notbeook.
