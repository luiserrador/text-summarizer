# End to end Text-Summarizer-Project

This project involves the implementation of a dialogue summarizer using the [pegasus model from Google](https://huggingface.co/google/pegasus-cnn_dailymail) pretrained with the [cnn_dailymail dataset](https://huggingface.co/datasets/cnn_dailymail). The model was fine-tuned to be able to summarize any conversation between two intervenients.

The dataset used to fine-tune the model was the publicly avilable [samsum dataset](https://huggingface.co/datasets/samsum). Different stages were implemented to prepare data for training (data ingestion, validation and transformation). 📊

One API was created using FastAPI, which can be accessed through a ASGI launched using uvicorn. This API allows model interaction, including training and prediction. 💻✨

The CI/CD process is also implemented using Docker and GitHub actions. A Docker container image is created and pushed to Amazon ECR. Then, the latest image is pulled to an Amazon EC2 instance running the application. GitHub Actions is responsible for automatically pulling the latest image to the EC2 instance. 🐳🚀

### TODO
* [ ] Frontend GUI;