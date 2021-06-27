### install kong 
use kustomize
```
kustomize build github.com/kong/kubernetes-ingress-controller/deploy/manifests/base | kubectl apply -f -
```
### install cert-manager
https://cert-manager.io/docs/installation/kubernetes/
* install cert-manager

### 创建 cert issuer
```
kubectl apply -f letsencrypt-cluster-issuer.yaml
```