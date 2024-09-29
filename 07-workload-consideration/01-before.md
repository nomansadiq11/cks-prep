# Before

## Before you download the image

- make sure software package is verified
- encourge the develop build small micro service with smcall base image
- with this steps, ensure you are not adding any softare to the cluster except that which has cleared static and dynamic scanning

## Before running containers

- static analysis
- a souce code use to build the container, look throught statements, declaration and possible errors in the code.
- further analysis can be performed after code build
- Dyanmic Analysis
- Dyanmic Admission controler to scan the images (sysdig and Aqua)
- but this will take 30 sec to scan the images before startup
- Aviation, reactor protection systems, and medical devices are some of the safety-critical systems where malicious or vulnerable code could have tragic effects.
- there are serveral tools can be use to scan the images
- Docker Bench, Clair, Trivy
