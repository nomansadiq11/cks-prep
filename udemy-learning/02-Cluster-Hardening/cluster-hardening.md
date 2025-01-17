# Cluster Hardening

## create the user for RBAC to ues

- we can create user with csr file and approve the request to allow access to the following user to connect with cluster
- create RBAC and assing to user which will allow user to communicate with kubeAPI

## ClusterRole and Clusterrole binding

- Clusterrole will use for full cluster
- you can also use rolebinding with clusterrole to allow for specfic permissions

## Ingress

- Ingress using for multiple application via one loadbalancer
- ingress resouce we define the rules how the request to route
- ingress controller works on layer 7,
- our loadbalaner route traffic to ingress controller
- use tls secret for certificate in ingress for specific domain like if you have some customer domain

## Service Account

- it's machine accounts like to for automation
- kubernets create service account by default
- token store in path /var/run/secret/kubernetes.io/serviceaccount
- if you create namespace service account will also created
- service accont have permission whatever to provide
- kubernete assing default SA to pod automaticaly if you don't define
- only allow to get the api curl command not other permission to allow
- automoutne service account to be false if you don't want to mount the service account
- if SA set automouncsa false but pod set automountSA true then SA will be mount to pod, pod will take precedence