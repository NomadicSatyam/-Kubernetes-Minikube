### Kubernetes Commands for Local Machine

Make sure Kubernetes is installed on the local machine.

```
minikube start
minikube status
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


