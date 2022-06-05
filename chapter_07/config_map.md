# Creating a ConfigMap

```
kubectl create configmap fortune-config --from-literal=sleep-interval=25

kubectl get configmap fortune-config -o yaml

apiVersion: v1
data:
  sleep-interval: "25"
kind: ConfigMap
metadata:
  creationTimestamp: "2022-06-05T17:53:13Z"
  name: fortune-config
  namespace: default
  resourceVersion: "36344"
  uid: 690db071-a439-43d6-871d-9dc39c1731e3
```

# Creating a ConfigMap from a file

```
kubectl create configmap my-config --from-file=config-file.conf
```

# Creating a ConfigMap from files in a directory

```
kubectl create configmap my-config --from-file=path/to/dir
```
