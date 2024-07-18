## create a namespace
```
kubectl create ns istio-action
// run as a default namespace
kubectl config set-context $(kubectl config current-context) --namespace=istio-action
```

