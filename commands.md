# Kubernetes Commands

## Pre-requisite
- kubectl Installation
- minikube Installation

## Run Locally

- Check minikube Status
    `minikube status`

- Start miniKube if not already running 
    `minikube start`

- Navigate to 'first' folder, deployment config file is deployment.yml
    `kubectl apply -f deployment.yml`

- Expose Service
    `kubectl expose deployment tomcat-deployment --type=NodePort`
    
- Get URL
    `minikube service tomcat-deployment --url`

- Stop minikube
    `minikube stop`

- Remove all clusters
    `minikube delate --all`


