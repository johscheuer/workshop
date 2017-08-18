# Monitoring

```bash
kubectl create namespace monitoring &> /dev/null
kubectl create -n monitoring configmap grafana-config --from-file=./dashboards/grafana-source.json
kubectl create -n monitoring configmap dashboards \
        --from-file=./dashboards/kubernetes-dashboard.json

kubectl apply -f ./
kubectl apply -f kube-state-metrics/
```
