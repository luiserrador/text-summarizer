# End to end Text-Summarizer-Project

This project involves the implementation of a dialogue summarizer using the [pegasus model from Google](https://huggingface.co/google/pegasus-cnn_dailymail) pretrained with the [cnn_dailymail dataset](https://huggingface.co/datasets/cnn_dailymail). The model was fine-tuned to be able to summarize any conversation between two intervenients.

The dataset used to fine-tune the model was the publicly avilable [samsum dataset](https://huggingface.co/datasets/samsum). Different stages were implemented to prepare data for training (data ingestion, validation and transformation). 📊

One API was created using FastAPI, which can be accessed through a ASGI launched using uvicorn. This API allows model interaction, including training and prediction. 💻✨

The CI/CD process is also implemented using Docker and GitHub actions. A Docker container image is created and pushed to Amazon ECR. Then, the latest image is pulled to an Amazon EC2 instance running the application. GitHub Actions is responsible for automatically pulling the latest image to the EC2 instance. 🐳🚀

## Dialogue Summarizer with Pegasus Model

This project implements a dialogue summarizer utilizing the [Pegasus](https://huggingface.co/google/pegasus-cnn_dailymail) model by Google, pretrained on the [CNN_DailyMail](https://huggingface.co/datasets/cnn_dailymail) dataset. The model has been fine-tuned to summarize conversations between two participants.

### Data Preparation

The [Samsum](https://huggingface.co/datasets/samsum) dataset, publicly available, was used for fine-tuning the model. Various stages were implemented for data preparation, including data ingestion, validation, and transformation.

### API Implementation

An API has been developed using FastAPI, accessible through an ASGI launched with uvicorn. This API facilitates interaction with the model, enabling training and prediction functionalities.

### CI/CD Process

Continuous Integration/Continuous Deployment (CI/CD) processes have been established using Docker and GitHub Actions. A Docker container image is created and pushed to Amazon ECR (Elastic Container Registry). Subsequently, the latest image is pulled onto an Amazon EC2 instance where the application is hosted. GitHub Actions automates the process of pulling the latest image onto the EC2 instance, ensuring seamless updates.

#### **Note: The CI/CD process is not currently supported, as I have shutted down the AWS services for this process due to cost of the process.**

### TODO
* [ ] Frontend GUI