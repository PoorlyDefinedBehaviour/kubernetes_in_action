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
