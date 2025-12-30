# k8s-cluster
Manifests and Tooling for a Kubernetes cluster (Minikube mostly)

## ArgoCD installation (Core)
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v3.2.3/manifests/core-install.yaml
