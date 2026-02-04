# AWS-SageMaker-ML-project
This repository contains an end-to-end Machine Learning workflow built using AWS SageMaker, S3, Boto3, and XGBoost, covering everything from data storage to model deployment and cleanup.
The project demonstrates how to train, deploy, evaluate, and manage a machine learning model on AWS while following best practices such as versioned data storage and cost control.

Project Overview
Built and trained an ML model using XGBoost on AWS SageMaker
Used Amazon S3 for dataset storage and versioning
Deployed the trained model as a real-time endpoint
Evaluated model performance using a Confusion Matrix
Cleaned up resources by deleting endpoints to avoid charges

Tech Stack
AWS SageMaker (Notebook Instance / Studio)
Amazon S3
IAM
Python
Boto3
NumPy
XGBoost
JupyterLab

Project Workflow:
1.  Environment Setup
Created an AWS SageMaker Notebook Instance
Assigned IAM role with required permissions for SageMaker and S3
Opened JupyterLab and created a Conda Python environment

2. S3 Bucket Creation & Data Storage
Created an S3 bucket programmatically using Boto3
Uploaded training and testing datasets to S3
Used S3 for data storage and versioning for future reuse

3. Data Loading & Preprocessing
Read data from S3 into the notebook
Converted data into NumPy format
Split data into training and testing sets

4. Model Building & Training
Used the XGBoost algorithm via SageMaker built-in containers
Pulled the XGBoost container image using SageMaker utilities
Constructed a SageMaker Estimator
Trained the model using the training dataset stored in S3

5. Model Deployment
Deployed the trained model as a real-time inference endpoint using SageMaker
Created a predictor object for model inference

6. Model Evaluation
Generated predictions on test data
Evaluated model performance using a confusion matrix

7. Resource Cleanup
Deleted the deployed SageMaker endpoint after evaluation
Ensured no unnecessary AWS resources remained to avoid extra costs

Key Outcomes: 
Successfully built and deployed an ML model on AWS SageMaker
Implemented cloud-based data storage and versioning
Demonstrated end-to-end ML lifecycle management
Followed cost-optimization best practices 

Notes:
This project is intended for learning and demonstration purposes and can be extended further using hyperparameter tuning, SageMaker Pipelines, or model monitoring.
