#k8s-gusetbook-example


## Steps to perform
__first start the k8s/OCP environment__
```
kubectl cluster-info
kubectl get nodes
```

```
kubectl create -f redis-master-controller.yaml
kubectl get rc
kubectl get pods
```

```
kubectl create -f redis-master-service.yaml
kubectl get services
kubectl describe svc/redis-master
```

```
kubectl create -f redis-slave-controller.yaml
kubectl get rc
```

```
kubectl create -f redis-slave-service.yaml
kubectl get services
```

```
kubectl create -f frontend-controller.yaml
kubectl get rc
kubectl get pods
```

```
kubectl create -f frontend-service.yaml
kubectl get services
```

```
kubectl describe service frontend | grep NodePort
kubectl describe svc/frontend
```

```
curl http://<sevicehostIP>:80
```

or use browser

