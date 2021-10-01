[![CircleCI](https://circleci.com/gh/cyberranjith/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/cyberranjith/project-ml-microservice-kubernetes/?branch=master)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Description of files in the project
1. config.yml: Circle CI Config YML file which defines the Circle CI Jobs
2. app.py: The main flask based application
3. Dockerfile: Defines the commands to setup and run a docker container
4. make_prediction.sh: Tests the Sklearn Prediction Home API and gets the home prediction
5. Makefile: Defines the commands to be executed for setting up a virtual environment, installing dependencies and linting the docker file and python app.
6. requirements.tx: Defines the dependencies for the python application, which must be referenced for installing them
7. run_docker.sh: Script to run docker container in local
8. run_kubernetes.sh: Script to run docker container with kubernetes
9. upload_docker.sh: Uploads the built docker image of the python application to docker hub repository

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

## Pre-requisites to run the app in local
1. Run Docker Container:
    - Docker
2. Run docker container in a Kubernetes cluster:
    - Kubernetes
    - Minikube
    - Kubectl

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `minikube start` and then followed by `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
