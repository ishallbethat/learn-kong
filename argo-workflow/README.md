### argo workflow 默认采用 https
https://github.com/Kong/kubernetes-ingress-controller/issues/69#issuecomment-725948548
全程 https 只能通过修改 service: argo-server。 增加  konghq.com/protocol: https 解决
 kubernetes kong -> argo-server 。目前只能
```
kubectl patch svc argo-server --patch "$(cat patch.yaml)" -n argocd
```
### enable sso
* create secret
```
kubectl apply -f secret.yaml
```
* patch argocd-dex-server
```
kubectl patch deployment argocd-dex-server --patch "$(cat patch-argocd-sever-dex.yaml)" -n argocd
```
* workflow-controller-configmap
```
kubectl patch configmap workflow-controller-configmap --patch "$(cat patch-configmap.yaml)" -n argocd
```