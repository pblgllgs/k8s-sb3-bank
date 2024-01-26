# K8S UI

## Deploy Kubernetes UI

```bash
kubectl apply -f dashboard-adminuser.yaml     
```

## Get accessToken

```bash
kubectl get secret admin-user -n kubernetes-dashboard -o jsonpath={".data.token"} | base64 -d
```

## Expose

```bash
kubectl proxy
```
