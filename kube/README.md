
# Kafka-WebView - Kubernetes manifests

## Important notes
- To simplify operations and maintenance, these manifests use [Kustomize](https://github.com/kubernetes-sigs/kustomize), see `kustomization.yaml` files
- `prometheusServiceMonitor.yaml` manifests refer to the [CoreOS Prometheus Operator](https://github.com/coreos/prometheus-operator) [ServiceMonitor](https://github.com/coreos/prometheus-operator/blob/master/Documentation/user-guides/getting-started.md#related-resources) resource
- in `kustomization.yaml` is set a sample Namespace named `kafka`, feel free to modify it ;)

---

## NO-SSL

### WITHOUT persistence
```shell
# deploy
kubectl apply -k kube/no-pvc/
# remove
kubectl delete -k kube/no-pvc/
```

### WITH persistence
```shell
# deploy
kubectl apply -k kube/pvc/
# remove
kubectl delete -k kube/pvc/
```

---

## HTTPS

`WORK IN PROGRESS`

### WITHOUT persistence
```shell
# deploy
kubectl apply -k kube/https/no-pvc/
# remove
kubectl delete -k kube/https/no-pvc/
```

### WITH persistence
```shell
# deploy
kubectl apply -k kube/https/pvc/
# remove
kubectl delete -k kube/https/pvc/
```
