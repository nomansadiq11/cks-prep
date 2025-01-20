# Minimize Microservice Vulnerabilities

## Admission Controller

- authentication --> authrorize --> admission controller --> kube objects
- validating: validate the pod should not create with priliviallage access
- mutating: adding or removing config base on the rule like, prod pods goes to node 2 and dev pods goes to node 1
- there are many admission controller look for website
- alwayspullImages: will add in the container always

## Security Context

- user shouldn't be root
- like volumen mount as root directory host system can read the host files
- runasuser, runasgroup and fsgroup should be use
- when you use these three attribue you cannot modify the files on the pods
- you can run docker into docker
- you can run docker --prilivage container to link with host devices
- you can create privillage container in kubernetw and you can access underlying resouces
- capsh --print to see the capabiliteis for that containers
- privillage container can be very dangrous

## ImagePullPolicy

- Always - pull image always
- if not present - if image pull
- never -

## Admission Controller ImagePolicyWebhook

- We can implement external validator for image, like to validate if the image pull poicy have latest tag to reject it
- use admision controller for it
- you can configure the validator server and enable in admission webhook

## Secrets

- secret to store the sensitive data
- secret value is base64
- store mount as volume store as file can be readable
- 