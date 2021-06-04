#K8s CLI:

## Get list of elements
`kubectl get all`
`kubectl get nodes`
`kubectl get pods`
`kubectl get services`
`kubectl get deployment`
`kubectl get replicaset`

`kubectl describe pod PODNAME`

Option "-o wide" for more information
Option "-o yaml" or "-o yaml " for more information in file

##Deployment
`kubectl create deployment NAME --image=image`
`kubectl delete deployment NAME`
`kubectl edit deployment NAME`
`kubectl expose deployment NAME --type=NodePort --port=PORT`
`kubectl apply -f my-deployment.yaml`


Explain of deployment abstraction layers :
- Deployment
- ReplicaSet
- Pod
- Container


##Pod
Pod nomenclature : <deployment_name>-<replicaset_name>-<pod_id>
`kubectl logs POD_NAME`
`kubectl exec -it POD_NAME - - bin/bash`


##Get IP of service
minikube service DEPLOYMENT_NAME --url


##Encode password
`echo -n 'root' | base64`


##Get info of cluser
`kubectl cluster-info`

##Get ip of public load balancer
`minikube service YOUR-SERVICE`


#Namespaces
kube-system -> for k8s components
kube-public -> for public resources without identification
kube-node-lease -> heartbeats/availability of nodes
default -> for default components created by us

#Add ingress controleur on minikube
`minikube addons enable ingress`


##Decode Base64
echo -n 'string' | base64

HELM v3


Create apache et php avec un ingress
Create Statefullset Mysql




#Start pod ephemeral
kubectl run busybox --image=busybox -it --restart=Never --rm -- echo 'hello world'




















-----------------------------------
### install hyperhit and minikube
`brew update`

`brew install hyperkit`

`brew install minikube`

`kubectl`

`minikube`

### create minikube cluster
`minikube start --vm-driver=hyperkit`

`kubectl get nodes`

`minikube status`

`kubectl version`

### delete cluster and restart in debug mode
`minikube delete`

`minikube start --vm-driver=hyperkit --v=7 --alsologtostderr`

`minikube status`

### kubectl commands
`kubectl get nodes`

`kubectl get pod`

`kubectl get services`

`kubectl create deployment nginx-depl --image=nginx`

`kubectl get deployment`

`kubectl get replicaset`

`kubectl edit deployment nginx-depl`

### debugging
`kubectl logs {pod-name}`

`kubectl exec -it {pod-name} -- bin/bash`

### create mongo deployment
`kubectl create deployment mongo-depl --image=mongo`

`kubectl logs mongo-depl-{pod-name}`

`kubectl describe pod mongo-depl-{pod-name}`

### delete deplyoment
`kubectl delete deployment mongo-depl`

`kubectl delete deployment nginx-depl`

### create or edit config file
`vim nginx-deployment.yaml`

`kubectl apply -f nginx-deployment.yaml`

`kubectl get pod`

`kubectl get deployment`

### delete with config
`kubectl delete -f nginx-deployment.yaml`

#Metrics

`kubectl top` The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, or for a particular pod or node if specified.

