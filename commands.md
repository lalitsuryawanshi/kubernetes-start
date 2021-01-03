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

## kubectl commands

- Get all pods
    `kubectl get pods`

- Get single pod
    `kubectl get pods <pod-name>`

- Describe pod
    `kubectl describe pod <pod-name>`

- Expose Deployment
    `kubectl expose deployment <deployment-name> <-port=external-port> <-target-port=container-port> <-type=service-type>`

- Port Forward
    `kubectl port-forward <pod-name> <local-port>:<remote-port>`

- Attach pod 
    `kubectl attach <pod-name> -c <container>`

- Execute command within deployment pod, get prompt within pod
    `kubectl exec -it <pod-name> bash`
    
- Exit from execute prompt `exit`

- Label pod
    `kubectl label pods <pod-name> KEY_1=VAL_1`

- Run Image
    `kubectl run <name> --image=<image-name> --port=<port-number>`

- Reference
    `https://minikube.sigs.k8s.io/docs/start/`



