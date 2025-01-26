# Monitoring, Logging and Runtime Security

## Falco

- Detection and prevention
- preveion is like securigy group acl
- it's opensource tool, allow to add rules
- like shell user logged in
- there are rules written in falco lib and which apply and monitoring the pods
- falco rules are written in yaml
- you can track which user doing in cat in side the containe3rs
- you can create custom macros like create reusble function
- you can define the list of proc to monitoring the rules, like macros
- format the logs in facol rule
- use awk to filter the column

## Sysdig

- we use log ot command troublehsott
- like strace, tcpdump, lsof, netstat, htop,iftop
- sysdig comes with own commans with interface (csysdig)
- install sysdig and
- sysdig also support the containers
- csisdig is GUI to show the events
- sysdig track your commands also to see what users are doing on yoru system

## Audit Logging

- get the logging for the api servers
- like none, metadat, request, requestresponse, these rules can implemnt for audit policy
- we define the level of the policy like pod level or status level
- if you write new rule jut restart the kubeapi server
- restart the server by adding new lable to kube-api servers
- kubectl commands works on stage like (requet reced, response stated , respomnse complete panic if occord )
- audito log you can exaclty see the same logs like secrets also
- you can omitstages from the audit logs
- write the rules in the sequence to achive your goal

## Container Immutability at containerRuntime

- make container to readonly rootfilesystem by adding securitycontext

## Commands

- sysdig -> get the system commands running by process
- falco --> which track the rule bases on containers
