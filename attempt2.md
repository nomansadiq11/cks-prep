# Attempt 2

1 Cilium policy L4 and L3 with mutual auth
2 mahcine have developer user remove it from docker group and docker .sock file should have root permission
3 retricted namespace, there is deployment file update this and create deployment in that namespace
4 SOBOM the docker image, there are 3 container in the depoyment file find package libcryptoo3 which image using it and do SBOM
5 cluster upgrade
6 imagewebhook configure it and create deployment which shouldn't work, enable all admission plugins
7 audit policy configuration and change the policy
8 create secrete from files, there is exsisting depployment already using it
9 kube api unauth, secure it and run it
10 kubelet anaoymouse configured, securte it
11 there are three deployment running, one of them using /dev/mem path, find the pod and find the deployment and make the replicas set to 0
12 create ingress and configure the TLS and redirect to https
13 service account configure automount disabled and mount the token path in the dpeloyment
14 network policy configure block ingress for namespace A and allow ingress from NA-A to NA-B only
