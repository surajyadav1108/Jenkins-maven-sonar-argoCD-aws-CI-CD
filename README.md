# CI/CD Pipeline for Maven Application Deployment with Jenkins, Maven, SonarQube, and Docker on AWS EC2 and ArgoCD on Local Minikube Cluster
## Project Description
### Overview
This project aims to establish a robust Continuous Integration and Continuous Deployment (CI/CD) pipeline for deploying a Maven-based Java application onto an AWS-hosted EC2 instance. The pipeline leverages various DevOps tools such as Jenkins, Maven, Docker, SonarQube, and an AWS EC2 instance to automate the build, test, and deployment processes. Additionally, it employs a local Minikube Kubernetes cluster to host ArgoCD for managing Kubernetes deployments. This end-to-end pipeline ensures a seamless and efficient software delivery process.

## Project Components
### 1. Jenkins
Jenkins serves as the central orchestration tool for the CI/CD pipeline. It automates build, test, and deployment stages and is responsible for triggering pipeline executions.

### 2. Maven
Maven is used for managing project dependencies, building the Java application, and packaging it into a deployable artifact.

### 3. SonarQube
SonarQube is utilized for code quality analysis. It scans the codebase and provides actionable insights to improve code quality.

### 4. Docker
Docker is employed for containerizing the application, ensuring consistency between development and production environments.

### 5. AWS EC2 Instance
An AWS EC2 instance is used to host Jenkins, Maven, SonarQube, and Docker. This instance acts as the primary build and CI/CD environment.

### 6. Minikube Kubernetes Cluster
Minikube is utilized to set up a local Kubernetes cluster. This cluster is used to host ArgoCD, which manages the deployment of Kubernetes resources.

## Key Pipeline Stages
The CI/CD pipeline consists of the following key stages:

### Code Commit: Developers commit code changes to the version control system (e.g., Git).

### Continuous Integration (CI):

Jenkins monitors the code repository for changes.
Jenkins triggers a Maven build for the application.
Unit tests and code quality checks are performed during the build process.
Docker images are built and tagged.

### SonarQube Analysis:

Jenkins triggers a SonarQube analysis to assess code quality.
Issues and code quality metrics are reported.

### Docker Image Registry:

Docker images are pushed to a Docker image registry (e.g., Docker Hub or a private registry).

### Continuous Deployment (CD):

ArgoCD, running on the local Minikube cluster, watches the Git repository for changes in Kubernetes manifests.
When changes are detected, ArgoCD synchronizes the local Kubernetes cluster to match the desired state.

### Application Monitoring:

Set up monitoring and logging for the deployed application using tools like Prometheus and Grafana on the Minikube cluster.

### Scaling and Rolling Updates:

Utilize Minikube Kubernetes scaling features for managing application replicas.
Implement rolling updates to minimize downtime during deployments.

## AWS Infrastructure
An AWS EC2 instance is used for hosting Jenkins, Maven, SonarQube, and Docker.
Local Minikube Cluster

## A local Minikube Kubernetes cluster is set up for hosting ArgoCD.
## Goals
Achieve a fully automated CI/CD pipeline.
Ensure code quality and security with SonarQube analysis.
Achieve version-controlled deployments with ArgoCD.
Implement scalability and high availability with Kubernetes on Minikube.
