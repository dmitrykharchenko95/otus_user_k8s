# otus_user_k8s

```shell
# prometheus stack
helm install stack prometheus-community/kube-prometheus-stack -f prometheus/prometheus.yaml

kubectl port-forward service/prometheus-operated  9090
kubectl port-forward service/stack-grafana 3000:80

```

```shell
helm install otus-user ./otus-user

kubectl port-forward service/user-service  8000
```

# Tests

```shell
newman run postman/otus_user.postman_collection.json
```
