[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Funmibi-A/project4_udacity/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Funmibi-A/project4_udacity/tree/main)

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

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally 
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl `kubectl run ml-api --image=$dockerpath `


Explanation of file directorys 

| Directory  | Description  |
| ------------- | ------------- |
| Circleci  | Contains config.yml file for circleci  |
| Model Data  | Showing housing prices in the boston area  |
| Output_files | Showing docker and kubernetes log outputs |
| app.py | REST endpoint in flask containing containing routes to fetch house prices in boston |
| Dockerfile | Docker creation files with dependencies |
| make_predictions.sh | Call to log output predictions from the REST api end point |
| Makefile | to install project dependcies and lint |
| requirements.txt | Python dependencies for the project |
| run_docker | shell script to build the docker file |
| run_kuberbetes | shell script to run and start up docker image in kubernetes | 
| upload_docker | shell script to upload locally built image to docker hub | 
