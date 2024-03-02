# Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD, Helm and Kubernetes

![argocd](https://github.com/Ranaahmedit/End-to-End-CI-CD/assets/127610751/6186c66b-f54b-4fbd-911b-731305d5b88f)

Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD, Helm, and Kubernetes:


   ### Before you run  
- Preparing the environment:
   - Jenins server installed and running.
   - Java application code hosted on a Git repository.
   - Maven and Docker are installed on the Jenkins server.
   - Docker Hub account for pushing Docker images.
   - SonarQube server for static code analysis.
   - GitHub repository for source code and version control.
   - Kubernetes cluster for deployment.
   - Helm package manager for Kubernetes.
## Jenkins Setup

### Install Jenkins Plugins

- Install the necessary Jenkins plugins, including Git, Docker Pipeline, and SonarQube Scanner.

### Create Jenkins Pipeline

- In Jenkins, create a new pipeline job.
- Configure the pipeline with the Git repository URL where the Java application code is hosted.
- Add a Jenkinsfile to the Git repository to define pipeline stages.
        
    - Define Pipeline Stages:
       ## Pipeline Stages
      
### Stage 1: Checkout Source Code

- Checkout the source code from the Git repository.

### Stage 2: Build the Application

- Build the Java application using Maven.

### Stage 3: Static Code Analysis

- Run SonarQube analysis to check the code quality.



   ![sonarqube1](https://github.com/Ranaahmedit/End-to-End-CI-CD/assets/127610751/11d2186f-f7c3-4e2b-b7a8-6ffc960eadbe)
  

### Stage 4: Build and Push Docker Image

- Build a Docker image from the application.
- Push the Docker image to Docker Hub.

  
    ![dockerhub ](https://github.com/Ranaahmedit/End-to-End-CI-CD/assets/127610751/f5ffdbeb-903e-477b-a7f1-7a4dea42e071)
  

### Stage 5: Update Deployment File

- Update the deployment file (e.g., deployment.yaml) with the new Docker image version.
- Commit the changes to the Git repository and push to GitHub.
                       ---------------------------------------------------------------------------------------------------------------------------


  - CI Pipeline:

      ![jenkins1](https://github.com/Ranaahmedit/End-to-End-CI-CD/assets/127610751/54789846-653d-4779-849c-0b1c84454f86)





      Note: Ensure all necessary credentials are configured in Jenkins, such as Docker Hub credentials, SonarQube token, and GitHub token.








- Install Argocd in minikube cluster
  
    ![argocd](https://github.com/Ranaahmedit/End-to-End-CI-CD/assets/127610751/d5c13480-3881-43dd-9674-823470b65a49)


This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD, Helm, and Kubernetes.
