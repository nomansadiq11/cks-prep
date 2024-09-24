# Limiting the Connection Rate

- limit the ssh connection rate
- like you can limit the per connection per ip
- like drop the connection after 10 minutes

## EventRate Limit

- we can enable this in admission controller by default this is disable
- this limit keep the cluster health stable
- like By limiting the rate of events, this admission controller helps ensure the stability and performance of the cluster.

## Ingress Controller

- Kubernetes not allow to communicate low number or port,
- by chance require for such ports, there are ingress controller exists which help to solve this problem
- ingress controller maybe have different features, but they don't have wide range or monitoring features

## Secure Ingress

- it's exposes HTTP and HTTPs routes from outside the cluster to services within the cluster.
- for https we can use certicate and key file to secure the communicate between client load balancer using TLS.
