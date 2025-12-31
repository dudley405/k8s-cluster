# k8s-cluster
Manifests and Tooling for a Kubernetes cluster (Minikube mostly)


## Resources:
Prometheus  
Grafana   
Loki  
Alloy


## Argo
Provisions basic monitoring (metrics, logs) for a local Kubernetes cluster:
![dashboard.png](assets/dashboard.png)

![metrics.png](assets/metrics.png)

![logs.png](assets/logs.png)



### ArgoCD installation (Core)
kubectl create namespace argocd  
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v3.2.3/manifests/core-install.yaml

### Dashboard
argocd admin dashboard -n argocd
![](./assets/argo_ui.png)

### Alloy ConfigMap
kubectl create configmap --namespace monitoring alloy-config "--from-file=config.alloy=./config.alloy"

