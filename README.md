## Install
bash
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl port-forward --address 0.0.0.0 svc/argocd-server -n argocd 8080:443
```

Login
```
kubectl get secret argocd-initial-admin-secret -n argocd -o yaml
echo "secret" | base64 decode
```