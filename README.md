[![CircleCI](https://circleci.com/gh/Goddhi/DevOps_Microservices_Project.svg?style=svg&circle-token=<YOUR_STATUS_API_TOKEN>)](https://app.circleci.com/pipelines/github/Goddhi/DevOps_Microservices_Project)

<h2>Project Overview </h2>

<p>The Operationalize ML project contains a Machine Learning Microservice, built on Scikit-Learn. It contains a model that predicts house prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 
</p>

<h3>Project Tasks</h3>

- Run a docker container<br>
- Upload container into a public registry (hub.docker.com)<br>
- Run the deployed application in a Minikube Kubernetes cluster<br>
- Integrate with CircleCI for continuous integration<br>

<h3>Setup the Environment</h3>

<h4>Requirements</h4>
  Python 3.7
  
 - <h3>Steps</h3>
   - Fork this repo and clone it to your local machine

    - <h4>Step 1: Install dependencies</h4><br>

    - Set up the environment by running make setup. This will create a virtual environment in your home directory called .devops<br>
    - Install dependencies by running `make install`<br>
    - (Optionally) Lint application (requires hadolint)<br>

    <h4>Step 2: Run Docker container</h4>

    - Run the application on docker by calling `./run_docker.sh`

    <h4>Step 3: Upload to Docker Hub</h4><br>

    - In the ./upload_docker.sh file, edit the dockerpath (line 8) and change the docker  username to a personalized one daredrexel/ml-api <br>
    - To upload to docker hub, run `./upload_docker.sh`<br>

    <h4>Step 4: Kubernetes deployment</h4> <br>

    To deploy to kubernetes, run `./run_kubernetes.sh`

   

