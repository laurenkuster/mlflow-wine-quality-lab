# MLflow Wine Quality Experiment Tracking Lab

This project demonstrates experiment tracking and model management using **MLflow**.  
The goal of the lab was to train machine learning models to predict wine quality and use MLflow to track experiments, compare models, and register the best performing model.

## Project Overview

The starter notebook originally trained a **Random Forest model** and logged the experiment with MLflow.  
To extend the lab, I added an additional model (**Logistic Regression**) to compare performance across different algorithms.

Both models were trained and logged using MLflow so their parameters, metrics, and artifacts could be compared in the MLflow UI.

## Models Implemented

Two models were trained and evaluated:

- **Random Forest Classifier**
- **Logistic Regression**

Each run logged the following information to MLflow:

- model parameters
- training metrics
- trained model artifacts

Using MLflow made it easy to compare the results of both models and determine which performed better on the dataset.

## MLflow Experiment Tracking

MLflow was used to:

- track experiment runs
- log model parameters
- log evaluation metrics
- store trained models
- register the best model in the **MLflow Model Registry**

The MLflow UI was used to visualize and compare the experiment results.

## Spark Removal

The original notebook included setup for **Spark**, but Spark was not necessary for this experiment since the dataset is small and the models were trained using **scikit-learn**.

To simplify the workflow and avoid unnecessary dependencies, the Spark components were removed and the experiment was run entirely with standard Python libraries.

This made the notebook easier to run locally and reduced setup complexity.

## Running MLflow UI

To view the experiment results:

```bash
python -m mlflow ui --backend-store-uri ./mlruns --port 5000
