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

![Architectural Diagram](/screenshots/Architectural Diagram.png =950x)

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

![Dataset](/screenshots/dataset.PNG =950x)