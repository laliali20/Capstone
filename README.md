# Capstone

## Generating Product Price Recommendations For Revenue Optimization

This repo contains code and other resources for a model that forecasts the number of visits for wikipedia articles as well as the goodle trend expected over the next one year.


### About the project 

The goal of the competition was to generate recommendations for a self storage company that make market sense based on the observed trends in the market as well as to provide a snapshot performance indicators dashboard.

The data is from two sources. The first source is Prorized owned data which is mainly used as competitor data. The second is a simulation of rentals in one facility done on Rockwell Arena Simulation.


### Contents
* [Overview](#overview)
* [Technologies](#technologies)
* [Setup](#setup)
* [Notebook](#notebook)


### Overview
Daily rental data is initially simulated and then saved into an excel sheet. 

The next step is to format it into a monthly time series. This becomes the input into the forecast models. 

The forecast model is picked out based on a holdout sample approach, where the perforrmance of the test set is evaluated on the MAPE accuracy metric. 

The best performing model is applied to give the 1 month prediction, which is an input of the optimization process.

The other input is the reference price computation. This is computed from the Prorize LLC data which contains historical web prices.

The forecast and reference price are used as the optimization inputs to generate recommendations.

### Notebook
The code and report for training and forecasting on the google trend and wikipedia page visits is in this [notebook](https://colab.research.google.com/drive/1HGJQR_f1p5-kdnkU_ayCKZYZOEqcJWLL?usp=sharing)

#### Performance Models Used
The performance ofthe models applied is evluated based on Mean Absolute Percenta Error (MAPE) 

### Summary
Recommendations are generated on the colab notebook. 

All processing necessary for the analytics is done within the notebook as well. 

Dashboard containing these metrics is prepared on PowerBi.

Challenges faced in the project are summarized in the conclusion section of the notebook.
