### Kubernetes Commands for Local Machine

Make sure Kubernetes is installed on the local machine.

```
minikube start
```

```
minikube status
```

```
minikube dashboard

```

Command to delete Minikube:

```
minikube delete

```

### Deploying Nginx App

Create a deployment for the Nginx app using the Nginx image:

```
kubectl create deployment my-nginx --image=nginx:latest

```

Commands to check deployment and pod status:

```
kubectl get deployment

```
```
kubectl get pods
```

Command to delete deployment:

```
kubectl delete deployment my-nginx
```

Commands for port binding, service creation, and usage:

```
kubectl expose deployment my-nginx --port=80 --type=LoadBalancer
```
```
kubectl get services
```
```
minikube service my-nginx
```


## Deploying Custom Web App

Create a deployment using a custom remote image:

```
kubectl create deployment my-webapp --image=satyambrother/dropdown-menu:02
```

Commands to check deployment, pods, and logs:

```
kubectl get deployment
```

```
kubectl get pods
```
```
kubectl logs <pod-Name>
```
```
kubectl describe pods
```

Command to create a service:

```
kubectl expose deployment my-webapp --type=LoadBalancer --port=3000
```

Commands to execute service and modify services:

```
minikube service <service-name>
```
```
kubectl patch service my-webapp -p '{"spec": {"type": "LoadBalancer"}}'
```

```
kubectl get services
```

```
minikube service my-webapp
```

## Rolling Updates and Rollback

Command to change deployment image for updates:

```
kubectl set image deployment my-webapp dropdown-menu=satyambrother/dropdown-menu:03
```

Commands for rollout and rollback:

```
kubectl rollout status deployment my-webapp
```
```
kubectl rollout undo deployment my-webapp
```


## Scaling and Deleting Deployments

Scale deployment to multiple instances:

```
kubectl scale deployment <deployment-name> --replicas=4
```

## Commands to delete deployments:

```
kubectl delete deployment <deployment-name>
```
```
kubectl delete deployment --all
```


Command to delete a service:

```
kubectl delete service <service-name>
```

## Executing YAML Files

Commands to execute deployment and service YAML files:

```
kubectl apply -f deployment-node-app.yml
```

```
kubectl apply -f service-node-app.yml
```

```
Command to delete deployment from YAML file:
```

```
kubectl delete -f deployment-node-app.yml
```

## Running Services
Run or execute a service running in Docker:

```
minikube service <service-name>
```

```
minikube service nodedb-service
```

## Other Useful Commands
Commands to get information:

```
kubectl get all
```

```
kubectl get sc
```
