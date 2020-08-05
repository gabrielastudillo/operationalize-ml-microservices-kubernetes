[![GAstudillo](https://circleci.com/gh/gabrielastudillo/operationalize-ml-microservices-kubernetes.svg?style=svg)](https://circleci.com/gh/gabrielastudillo/operationalize-ml-microservices-kubernetes)

## _Introduction_

The goal of this project is to operationalize a machine learning microservice using kubernetes, which is an open-source system for automating the management of containerized applications. In this project you will perform the following tasks:

- Test the project code using linting
- Complete a Dockerfile to containerize this application
- Deploy a containerized application using Docker and make a prediction
- Improve the log statements in the source code for this application
- Configure Kubernetes and create a Kubernetes cluster
- Deploy a container using Kubernetes and make a prediction

## _Instructions_

**1)** Using the console clone this repo:

__`git clone https://github.com/gabrielastudillo/operationalize-ml-microservices-kubernetes.git`__

**2)** Run this command to create a virtual environment and activate it:

__`make setup`__

**3)** Run this command to install the project dependencies:

__`make install`__

**4)** Run this command to lint the project files (python app and dockerfile):

__`make lint`__

**5)** Run this script to build a docker image for the app and start the app locally in a docker container:

__`./run_docker.sh`__

**6)** Run this script to obtain a prediction from the app running in the back:

__`./make_prediction.sh`__

**7)** Run this script to upload the docker image to your Docker hub account. Hint: Edit the scrip with your won docker hub account:

__`./upload_docker.sh`__

**8)** Run this script to run the service in a kubernetes cluster:

__`./run_kubernetes.sh`__

**9)** Run this script again to get a prediction from the app running in the cluster after port forwarding is active:

__`./make_prediction.sh`__

&nbsp;

## _Files:_

- app.py: The flask app that runs the service.
- Makefile: File that allows to automate common task for aasy setup of the project.
- Dockerfile: This file has the setup for creating a Docker image for the microservice.
- run_docker.sh: This script creates a docker image from the Dockerfile, list the images and starts a container.
- upload_docker.sh: This script uploads a docker image to your docker hub account.
- run_kubernetes.sh: This script runs the docker image in a kubernetes cluster (locally).
- make_prediction.sh: This script sends data for prediction.
