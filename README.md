# Robust Spatial Uncertainty Modeling Workflow Surrogate Flow Model

This repository contains a new and general workflow to generate accurate and precise machine learning-based surrogate flow models to predict the relationship between the reservoir rock and fluids, development parameters, and the reservoir flow simulation responses. We train a deep convolutional neural network using the results from a three-dimensional two-phase flow simulator. Next, we use the dropout hyperparameter to generate ensemble predictions from the flow surrogate to evaluate the accuracy and precision of the model. The machine learning-based surrogate model uses exhaustive subsurface predictor features, porosity, permeability, well position, and an engineered feature representing non-dimensional time as input to predict exhaustive subsurface response features, pressure, and saturation distribution over discrete time steps as the output. The proposed workflow integrates the spatiotemporal aspect of subsurface flow modeling. 

<p align="center">
<img src="https://github.com/emaldonadocruz/Images/blob/master/Saturation_sample.png" width="500px"></img>
</p>

## Executive summary

To evaluate uncertainty, we rely on multiple geostatistical subsurface heterogeneity realizations paired with flow simulation forecasts to test the sensitivity of various reservoir development parameters and build an uncertainty model of reservoir performance. However, with large reservoir models, numerical flow simulation time increases, leading to a significant amount of professional time and computational effort that increases project costs, and increases cycle times resulting in delay or diminished decision quality. This issue motivates the utilization of surrogate, computationally efficient approximative flow models. Current methods focus on prediction accuracy and minimizing prediction error. When uncertainty is significant, prediction accuracy is insufficient, and we must consider the entire uncertainty distribution. 
We propose a new and general workflow to generate accurate and precise machine learning-based surrogate flow models to predict the relationship between the reservoir rock and fluids, development parameters, and the reservoir flow simulation responses. 

## Data

For this notebook example we have prepared a dataset containing the results of a numerical flow simulator that considers a three dimension, two phase displacement problem.

<p align="center">
<img src="https://github.com/emaldonadocruz/Images/blob/master/Sample.png" width="500px"></img>
</p>

## Notebook contents

1. Executive summary
2. Objective
3. Introduction
4. Library importing
5. Functions
6. Dataset exploration
7. Dataset normalization and split
8. Deterministic prediction
    1. Model goodness evaluation
9. Uncertainty model generation
    1. Model goodness evaluation
10. Hyperparameter space exploration
    1. Summary of the training
11. Conclusions and observations

**NOTE**: The hyperparameter space exploration section might be too long to run, we have included the results of the grid search in Search-Space.pkl. Feel free to skip this section and load the results in Summary of the training subsection
