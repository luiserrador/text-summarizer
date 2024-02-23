# Dialogue Summarizer with Pegasus Model

This project implements a dialogue summarizer utilizing the [Pegasus](https://huggingface.co/google/pegasus-cnn_dailymail) model by Google, pretrained on the [CNN_DailyMail](https://huggingface.co/datasets/cnn_dailymail) dataset. The model has been fine-tuned to summarize conversations between two participants. 🤖

### Data Preparation

The [Samsum](https://huggingface.co/datasets/samsum) dataset, publicly available, was used for fine-tuning the model. Various stages were implemented for data preparation, including data ingestion, validation, and transformation. 📊

### API Implementation

An API has been developed using FastAPI, accessible through an ASGI launched with uvicorn. This API facilitates interaction with the model, enabling training and prediction functionalities. 🚀

### CI/CD Process

Continuous Integration/Continuous Deployment (CI/CD) processes have been established using Docker and GitHub Actions. A Docker container image is created and pushed to Amazon ECR (Elastic Container Registry). Subsequently, the latest image is pulled onto an Amazon EC2 instance where the application is hosted. GitHub Actions automates the process of pulling the latest image onto the EC2 instance, ensuring seamless updates. ⚙️

#### **Note:** _The CI/CD process is not currently supported, as I have shutted down the AWS services for this process due to costs._ 🚫🔧

### TODO
* [ ] Frontend GUI