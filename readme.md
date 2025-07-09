
https://github.com/argoproj/argo-helm/tree/main/charts/argo-cd

helm repo add argo https://argoproj.github.io/argo-helm
helm install -f charts/values-argo.yaml argo argo/argo-cd -n argocd --create-namespace

k port-forward svc/argo-argocd-server 8080:80 -n argocd