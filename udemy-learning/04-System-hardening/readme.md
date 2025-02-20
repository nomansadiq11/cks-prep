# System Hardening

## DAC (Discretionary Access Control)

- allow access to files base on the group  and subject

## Mandatory Access Control

- SElinux one of the famous control
- confined = not trusted and unconfied = trusted
- you can create script and add to apparmor profile which will enforce
- there are two mode in apparmor enforce and constraint
- enforce = force the policy
- constraint = audit the violation policies

## AppArmor Integration with kubernetes

- create profile in apparmor
- add to the annodation add the profile anme
- if the apparmor profile doesn't exists, the pod status will be block state

## OCI (Open Container Initiative) and Containers runtime
- OCI
    - two important specs
        - image specification
            - how to create image
        - Runtime Specs (like docker, podmain and containerd)
    - cri - contaienr runtime interface, which will communicate with OCI

## Configure the containerd and runc

- you can find the documentation for configure these in kubernetes
- we can install containerd and with runc
- we can create container using runc
- with ctr command we can pull the image

## CRI (Container runtime Interface)

- cri-o
- contaienrd
- docker
- kubelet no need to recompile
- install kubeadm then kubelet

## Container Runtime Sandboxes

- dmesage is a command on most Unix like operation system that print the message buffer of the kernel
- gvisor is another layer top of the kernal which have limited number of access
- application running on machine can take advange of the kernal bugs
- limit the application config using secComp
- then they introduce the gvisor
- gvisor nornal, limited syscall
- if we depoy pods base on gvisor the dmesag output will be limited

## Implementing RunTimeclass - gVisor

- there is default runtimeclass which run nornally like kernal with runc
- we can create new runtimeclass with gvisor which uses the runsc

## Kubeadm and Calcio

- kubeadm to install/upgrade kubernetes components
- calcio is network plugin

## Network Policies

- creating the network policy in namespacew will impact only that namespace
- kubectl get netpol
- if outbound not allowed but stateful of the request will works
- we can add netpol to specfic the pods by using the labels
- allow from ns and specfic role, label the namespace
- you can desscribe the netpol and see the output what netpol will do this
- if some pod compromised you can create netpol to block all the network ingress and egress
- pod selector means which pod this network policy gonna apply

## Commands

- aa-status {get the status of the apparmor}
- apparmor_parser {profile name} - configure the profile to app armor