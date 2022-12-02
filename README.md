## Install ArgoCD in k8s

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

## Access ArgoCD UI

```
kubectl get svc -n argocd
kubectl port-forward svc/argocd-server 8080:443 -n argocd
```

## Aogin with admin user and below token (as in documentation):

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo
```
## Apply Configuration to ArgoCD

```
kubectl apply -f application.yaml
```
