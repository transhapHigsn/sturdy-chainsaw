# sturdy-chainsaw
Learning K8s using microk8s


## Deploy a caddy server using microk8s on single node kubernetes cluster

1. RUN ```microk8s.kubectl apply -f caddy-deployment.yml```
2. RUN ```microk8s.kubectl expose deployment caddy-demo --type=LoadBalancer --name=my-caddy-service```
3. RUN ```microk8s.kubectl describe services my-caddy-service```
4. Now, visit url mentioned by endpoint field.


Note: I was trying to expose service NodePort ```(using caddy-service.yml configuration)```, but was not able to implement that correctly. So, i switched to above expose method.

Note: To install `microk8s`, refer to this [link](https://microk8s.io/docs/)
