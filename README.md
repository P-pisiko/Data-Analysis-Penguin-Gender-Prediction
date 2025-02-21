# Penguin Gender Prediction Project

## Overview
This project uses the Penguin dataset from the Seaborn library to analyze and predict their gender based on physical properties. Using Logistic Regression, the model aims to predict the gender of the penguins with 97% accuracy.

## Dataset

The dataset contains information about penguins, including the following features:

- Species
- Bill Length
- Bill Depth
- Flipper Length
- Body Mass
- Sex

## Data Cleaning
The dataset is sanitized to prepare the data with the following steps:
### Cleared Missing Values
- Removed rows with NaN values to improve performance
- Improved the accuracy of the Logistic Regression model

### Removed Irrelevant Column
- `island`: No impact on gender

### Data Transformation
Converted categorical data to numerical values:
- sex: male → 0, female → 1
- species: Adelie → 0, Chinstrap → 1, Gentoo → 2

## Web Service

The model can be interacted with **web requests**, and the service is done with **Flask**.

Endpoints:
- `/penguin/sample`: gets a sample data from the server.
- `/penguin/explain`: returns an object explaining the values users can provide to get a prediction from the model.
- `/penguin/evaluate`: evaluates the sex of the penguin based on the provided properties.
