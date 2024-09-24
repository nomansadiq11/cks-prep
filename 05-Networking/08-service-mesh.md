# Service Mesh

- service mesh are built with security as a main goal, and have submitted to outside security audits and investigations.

## Cilium Service Mesh

- with this option, user have option to run service mesh without or with sidecar

## mTLS

- there are some communication happending non-http ports, so there will be security issue, than mtls come to the picture and take the advantage of this.

## Wireguard

- it's easy to use encrypted VPN with calico
- wire guard is a communication protocol, it's create virtual network with calico clusters
- this build for speed and security
- as layer 3 tunnel, wireguard removes the need for IPsec

## Network Polices

- by default kubernetes cluster all pods can seen each other
- we can implement the network policy for ingress and egress rule
- the use case is that, there could be multi-tanant producs, this only needs to access for specific peoples

examples are here [https://github.com/ahmetb/kubernetes-network-policy-recipes](https://github.com/ahmetb/kubernetes-network-policy-recipes)
