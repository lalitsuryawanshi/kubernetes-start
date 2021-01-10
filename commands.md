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

- Expose Service and Add Load Balancer
    `kubectl expose deployment tomcat-deployment --type=NodePort`
    `kubectl expose deployment tomcat-deployment --type=LoadBalancer`

- Describe Service
  `kubectl describe services tomcat-load-balancer`

- Scale Deployment
    `kubectl scale --replicas=4 deployment/tomcat-deployment`

- Get URL
    `minikube service tomcat-deployment --url`

- Get Deployment
    `kubectl get deployments`

- Change Image
    `kubectl set image deployment/tomcat-deployment tomcat=tomcat:9.0.1`

- Get Rollout Status
    `kubectl rollout status deployment tomcat-deployment`

- Get rollout history
    `kubectl rollout history deployment/tomcat-deployment`

- Get rollout details
    `kubectl rollout history deployment/tomcat-deployment --revision=4`

- Stop minikube
    `minikube stop`

- Remove all clusters
    `minikube delate --all`

## kubectl commands

- Get nodes
  `kubectl get nodes`

- Label node
    `kubectl label node <nodename> <label-name>=<label-value>`

- Get all pods
    `kubectl get pods`

- Get single pod
    `kubectl get pods <pod-name>`

- Describe pod
    `kubectl describe pod <pod-name>`

- Expose Deployment
    `kubectl expose deployment <deployment-name> <-port=external-port> <-target-port=container-port> <-type=service-type>`
    `kubectl expose deployment tomcat-deployment --type=NodePort`

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

- Run Proxy
    `kubectl proxy`

- Kubernetes Dashboard
    `minikube dashboard` (use locally)
    `http://localhost:8001/api/v1/namespaces/kube-system/services/kubernetes-dashboard/proxy`

- If the dashboard is not installed, get it here
    `kubectl create -f https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/recommended/kubernetes-dashboard.yaml`

### kubectl scale

- Scale Deployment
    `kubectl scale --replicas=4 deployment/tomcat-deployment`




- Reference
    `https://minikube.sigs.k8s.io/docs/start/`



