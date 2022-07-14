[![CircleCI](https://circleci.com/gh/Goddhi/DevOps_Microservices_Project.svg?style=svg&circle-token=<YOUR_STATUS_API_TOKEN>)](https://app.circleci.com/pipelines/github/Goddhi/DevOps_Microservices_Project)

<h2>Project Overview </h2>

<p>In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API.

You are given a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the data source site. This project tests your ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.</p>

<h3>Project Tasks</h3>

Your project goal is to operationalize this working, machine learning microservice using kubernetes, which is an open-source system for automating the management of containerized applications. In this project you will:

Test your project code using linting
Complete a Dockerfile to containerize this application
Deploy your containerized application using Docker and make a prediction
Improve the log statements in the source code for this application
Configure Kubernetes and create a Kubernetes cluster
Deploy a container using Kubernetes and make a prediction
Upload a complete Github repo with CircleCI to indicate that your code has been tested.

<h3>Setup the Environment</h3>

    Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv.

        python3 -m pip install --user virtualenv
        # You should have Python 3.7 available in your host. 
        # Check the Python path using `which python3`
        # Use a command similar to this one:
        python3 -m virtualenv --python=<path-to-Python3.7> .devops
        source .devops/bin/activate

     Run make install to install the necessary dependencies

<h3>Running app.py</h3>    

    1. Standalone: python app.py
    2. Run in Docker: ./run_docker.sh
    3. Run in Kubernetes: ./run_kubernetes.sh

<h3>Kubernetes Steps</h3>    
    Setup and Configure Docker locally
    Setup and Configure Kubernetes locally
    Create Flask app in Container
    Run via kubectl kubectl run ml-api --image=$dockerpath


<h3>Explanation of file directorys</h3>

.circleci: contains config file to run job that test the dockerfile for errors

MOdel_data: Showing housing prices in the boston area

output_txt_files: Showing docker and kubernetes log outputs

app.py: REST endpoint in flask containing containing routes to fetch house prices in boston

Docker: Docker creation files with dependencies

make_predictions.sh: Call to log output predictions from the REST api end point

makefile: to install project dependcies and lint

requirements.txt: Python dependencies for the project

run_docker.sh: shell script to build the docker file

run_kubernetes.sh: shell script to run and start up docker image in kubernetes

upload_docker: shell script to upload locally built image to docker hub

