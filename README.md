# Running a container on k8s

kubectl run kubia \
--image=poorlydefinedbehaviour/kubia \
--port=8080 \
--template=run/v1

kubectl create replicationcontroller \
--image=poorlydefinedbehaviour/kubia \
--port=8080

kubectl create deployment kubia \
--image=poorlydefinedbehaviour/kubia \
--port=8080

# Creating a service object

kubectl expose rc kubia --type=LoadBalancer --name kubia-http

# Describing a replication controller

kubectl describe replicationcontroller

# Seeing logs from a pod

kubectl logs {{pod_name}}

# Seeing logs from a container

kubectl logs {{pod_name}} -c {{container_name}}

# Port forwarding

<!-- port forwarding my port 8888 to port 8080 in the pod -->

kubectl port-forward kubia-manual 8888:8080

# Adding annotations

kubectl annotate pod kubia-manual mycompany.com/someannotation="foo bar"

kubectl describe pod kubia-manual | grep Annotations
