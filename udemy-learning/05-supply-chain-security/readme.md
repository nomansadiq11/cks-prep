# Supply Chain Security

## Vulnerability, Exploit and Payload

- vulnerability is hold in applciation
- exploit is the person
- payload, what robber will do

## Container Security Scanning

- scan the docker/container images
- there are many tools
    - anchor
    - trivey
    - Tenable
    - Docker Trust Registry
- it will give you list of package and then you see how to fix

## Trivy

- scan the image trivy image {image name} which will get you output of the scan results

## Kube-bench

- kube-bench validate the CIS benchmark, deployed resouces to kubernetes
- this will shows the remidiattion also how to fix the issue
- it's should be install all the nodes

## Static Analysis

- checkov can perform the static analysis
- you can see, shouldn't be using root user
- host filesystem shouldn't be mount
-