# otus_user_k8s

```shell
# prometheus stack
helm install stack prometheus-community/kube-prometheus-stack -f prometheus/prometheus.yaml

helm install otus-user ./otus-user

kubectl port-forward service/prometheus-operated  9090
kubectl port-forward service/user-service  8000
kubectl port-forward service/stack-grafana 3000:80

```

# Postman

Collection is in ./postman