# kube-apiserver

- as kube-api server validate the api requests
    - Authentication
    - Authorization
    - Admission Control



## kube api server yaml file

- command to pass kube-apiserver than there are many arguments
-

## variables
- --advertise-address
    - This address is the one used by the entire cluster. If this variable is not set, it will use the bind-address variable. If that is not set, it will use the default interface of the host.
- --allow-privileged
    - Privileged containers are not isolated; they share a namespace with the host, and have near full root privilege on the host. If not set, it defaults to false. As kubeadm clusters default to being set to true, you may want to test full application functionality after changing the value.
- --authorization-mode
- --client-ca-file
- --enable-admission-plugins
- --enable-bootstrap-token-auth


### etcd name starting variables
- The lines starting with etcd allow the kube-apiserver to communicate with the etcd pod, as well as the port and IP address to use.


## Enable Audit logs

- Enabling auditing in Kubernetes is essential for several reasons, primarily for security, compliance, troubleshooting, and operational visibility
- kube api server will log all the api calls with their information.
- Every call is divided into three phases from when the call is received (RequestReceived), handling the call (ResponseStarted), and response call is made (ResponseComplete). Should there be an issue, there is also the possibility of a panic (Panic).

Each of the events is compared against rules in order. The first of one or more rules which matches will set the audit level for the event. The audit levels are:

None
Nothing sent to backend.
Metadata
Metadata, but not request or response body, sent to backend.
Request
Metadata and request, but not response body sent.
RequestResponse
Metadata, request, and response bodies sent to backend.

