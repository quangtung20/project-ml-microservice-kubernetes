[![CircleCI](https://circleci.com/gh/quangtung20/project-ml-microservice-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/quangtung20/project-ml-microservice-kubernetes)

## Project Overview

The Operationalize ML project contains a Machine Learning Microservice, built on **Scikit-Learn**. It contains a model that predicts house prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). 

### Project Tasks

* Test project code using linting
* Complete a Dockerfile to containerize this application
* Deploy containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction

## START HERE

### Step 1: Setup the Environment

* Create a virtualenv and activate it
Run command
python3 -m venv <your_venv>
source <your_venv>/bin/activate

### Step 2: Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Step 3: Run Docker container
- Run the application on docker by calling `./run_docker.sh`

### Step 4: Upload to Docker Hub
- In the `./upload_docker.sh` file, edit the dockerpath (line 8) and change the docker username to a personalized one (or leave it as is, to use the public kcemenike/microproject:v1.0.0)
- To upload to docker hub, run `./upload_docker.sh`

### Step 5: Kubernetes deployment
- To deploy to kubernetes, run `./run_kubernetes.sh`

### Files

* `output_txt_files/docker_out.txt` contains logs returned after running the app with Docker
* `output_txt_files/kubernetes_out.txt` containes logs and the prediction returned after running the app with Kubernetes(`run_kubernetes.sh`)
* `run_docker.sh` contains the steps to get Docker running the app locally
* `run_kubernetes.sh` contains the steps to get Kubernetes running the app locally
* `upload_docker.sh` contains the steps to upload the image to the Docker repository
