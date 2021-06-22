## enable github authentication
```
kubectl patch configmap argocd-cm --patch "$(cat patch-configmap.yaml)" -n argocd
```
## Troubleshootting
### too many redirects
https://discuss.konghq.com/t/ingress-for-argocd/8515/3
```
kubectl patch svc argo-server --patch "$(cat patch.yaml)" -n argo
```
