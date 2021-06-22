# argo workflow 默认采用 https
https://github.com/Kong/kubernetes-ingress-controller/issues/69#issuecomment-725948548
全程 https 只能通过修改 service: argo-server。 增加  konghq.com/protocol: https 解决
 kubernetes kong -> argo-server 。目前只能
```
kubectl patch svc argo-server --patch "$(cat patch.yaml)" -n argo
```