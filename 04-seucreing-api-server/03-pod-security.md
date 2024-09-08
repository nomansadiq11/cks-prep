# Pod Security Admission (PSA)

Pod Security Admission is a Kubernetes feature that provides a way to enforce security standards for pods in a cluster. It enables administrators to define and enforce security policies that can restrict the behavior and configurations of pods based on their security context.

Administrators can enforce security policies at the namespace level. Policies can be configured to apply to all pods within a namespace, ensuring consistent security practices.

There are three predefined policy levels: Privileged, Baseline, and Restricted. These levels offer different degrees of security enforcement, from least restrictive (Privileged), to most restrictive (Restricted).

There are three predefined enforcement modes:

Audit: Logs a policy violation without affecting the creation of the pod.
Warn: Logs a policy violation and returns a warning to the client, but does not block the pod creation.
Enforce: Blocks the pod creation if it violates the policy.