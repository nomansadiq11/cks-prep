# Cluster Setup

## CIS (Center of Information Security) Benchmarks for Hardending

- Go to CIS website and find which applicaton /cloud platform you wanted to hardened

## CIS for kubernetes

- kube-bench will use to scan the cluster
- controlplance harding care by the cloud provider

## Etcd DB Security

- by default data store in etcd db as plain text
- transport layer is http
- if you pass certificate then it will allow you to read and write in database

## Asymmtrics Keys Encryption

- using these keys to encryp the communication between client and server

## Access Control

- Auth --> Athen --> Admission Controller --> create object

## API server token auth

- shouldn't be using Token auth for api server

## Taint and Toleration

- you can taint the node by adding taint to node
- key=value:NoSchedule, PreferNoSchedule, NoExecuate
- remove the taint just add hypen like key=value:NoSchedule-
