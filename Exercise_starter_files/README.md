# Operationalizing Machine Learning

## Overview

This is an end-to-end machine learning project on Microsoft Azure where I have configured a cloud-based machine learning production model, deployed, and consumed it. Using the Bank Marketing Dataset, I trained a machine learning model leveraging the AutoML feature of Azure Machine Learning Studio, deployed it into production using Azure Container Instance (ACI) and consumed it using REST endpoints. I also created, published and consumed a pipeline to automate the whole process.

The project had following steps:

- Register Data on Azure Machine Learning Studio
- Set up configurations like compute cluster, type of machine learning task (in this case classification), exit criterion, etc
- Deploy the best model using ACI
- Enable logging and Application Insights
- Consume Model Endpoints and interact with deployed model using swagger UI
- Create and Publish a pipeline using Azure Python SDK with the aid of a Jupyter Notebook

## Project Architectural Diagram

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/Architectural%20Diagram.png)

## Future Work

- Use a parallel run step in the pipeline
- Test a local container with a downloaded model
- Using pipelines to automate the whole workflow from data preparation, to machine learning tasks and deployment
- Using the Apache Benchmark tool to set a measure of optimal performance

## Project Steps

### 1. Authentication

Install Azure ML extension to interact with Azure ML Studio, create Service Principal and associate it to specific workspace.

### 2. Dataset and Automated ML Experiment Run

Uploaded dataset on Azure ML Studio, create a compute cluster in Automated ML run.

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/dataset.PNG)

Experiment Completed

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/experiment%20completed.PNG)

Best Model

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/best_model.PNG)

### 3. Deploying Model and Enable Logging

Best model was deployed using Azure Container Instance and we can access endpoints through which other service can interact with our deployed model.
After deploying our best model, we can enable Application Insights and retrieve log.
The logs.py was used to enable application insights

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/logs.PNG)

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/app%20insight%20enabled.PNG)

### 4. Swagger Documentation

Azure provides a swagger.json URL that can be used to create a web site that documents the HTTP endpoint for a deployed model. Here we consumed our deployed model using swagger and displayed the contents of the API for the model as shown below:

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/swagger%20UI.PNG)

### 5. Consume Endpoints

Once the model is deployed, we use the python script endpoint.py provided to interact with the trained model and return an output (prediction) as shown below:

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/endpoint%20result.PNG)

### 6. Create, Publish & Consume Pipeline

Here we use the Azure Python SDK with the aid of Jupyter Notebook to create, publish, and consume a pipeline as shown below:
#### Pipeline Run

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/run%20pipeline.PNG)
#### Run Widget

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/run%20widget%20output.PNG)

#### Status Active

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/Status%20Active.PNG)

#### Rest Endpoint

![](https://github.com/hmza09/nd00333_AZMLND_C2/blob/master/Exercise_starter_files/screenshots/Rest%20Endpoint.PNG)

## Screen Recording

This [video](https://youtu.be/6_q4PQwXAtI) shows the entire process of the working ML application