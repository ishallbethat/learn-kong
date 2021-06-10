### install kong gateway
```
https://docs.konghq.com/gateway-oss/2.4.x/kong-for-kubernetes/install/
```
# set up echo server for testing purpose
```
kubectl apply -f https://bit.ly/echo-service
```

curl -I 34.80.52.205:80 

kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.3.1/cert-manager.yaml

# install cert-manager
https://cert-manager.io/docs/installation/kubernetes/
* install cert-manager
```
kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.3.1/cert-manager.yaml
```
* 如果使用 letsencrypt 创建 cluster issuer 
```
kubectl apply -f letsencrypt-echo.gebi.link.yaml
```