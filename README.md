
[![CircleCI](https://circleci.com/gh/TRETH/Operationalize_A_Machine_Learning_Microservice_API.svg?style=svg)](https://circleci.com/gh/TRETH/Operationalize_A_Machine_Learning_Microservice_API)

## Project Overview

In this project, I applied the skills that I have acquired in this course to operationalize a Machine Learning Microservice API. 

I have utilised a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

My project goal was to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project I implemented the following:
* Tested the project code using linting
* Completed a Dockerfile to containerize this application
* Deployed the containerized application using Docker and made a prediction
* Improved the log statements in the source code for this application
* Configured Kubernetes and created a Kubernetes cluster
* Deployed a container using Kubernetes and made a prediction
* Uploaded a complete Github repo with CircleCI to indicate that my code had been tested

The detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Short explanation of the files in this repository
* ./circleci/config.yml: CircleCI configuration file for coordinating the build pipelines.
* app.py: Python Flask App that implements a machine learning model and outputs predictions of Boston house prices based on a pretrained model.
* Dockerfile: A docker file for building the image.
* requirements.txt: Install dependencies required for this project.
* Makefile: Contains instructions on setup, install and lint testing.
* run_docker.sh: Contains instructions on creating a container and running the container locally.
* upload_docker.sh: Upload docker image to Docker.
* run_kubernete.sh: Run docker container locally on Kubernetes via minikube.
* make_prediction.sh: Requests predictions from app.py runnig locally on docker and locally on Kubernetes.
* /model_data: Contains pre-trained housing model.
* /output_txt_files: Contains log outputs from app.py runnig locally on docker and locally on Kubernetes.

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`
4. Upload Docker Image to Docker Hub: ./upload_docker.sh
5. Make a prediction: ./make_prediction.sh

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
