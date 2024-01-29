# K8S UI

## Deploy Kubernetes UI


```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
```

```bash
kubectl proxy
```

```bash
kubectl apply -f dashboard-adminuser.yaml
```

```bash
kubectl -n kubernetes-dashboard create token admin-user
```

```bash
kubectl apply -f secret.yaml
```

## Get accessToken

```bash
kubectl get secret admin-user -n kubernetes-dashboard -o jsonpath={".data.token"} | base64 -d
```
