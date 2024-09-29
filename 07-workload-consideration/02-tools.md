# Tools

## Docker Bench

- Docker bench is similar tool like kube-bench, which run scan on image without being part of kubernets

## Clair

- This is another tool which scan the container images
- Developed by Quay.io and owned by Red Hat
- The tools divides into two parts
- http interface, a Notifier and Notification Storage
- Clair core which handles the download the vulnerability information comparting against existing images.

### how clair will works

- The first phase is indexing, which begins with a manifest submitted to Clair. Clair uses this information to download the image layers, scan them, and generate an IndexReport.
- The second phase is matching, when an IndexReport is compared against known vulnerabilities. These are downloaded on a regular basis. Be aware that after starting Clair you may have to wait for the download before being able to match.
- The third phase is when a vulnerability is found within an IndexReport. Depending on the configuration of the notification, the notifier will take action.

## Trivy

- While Clair use alpine-secdb which covers back ported fixes
- clair may have half many issues as are currently discovered.
- Trivy is simple comprehensive tool to scan the images
- each time trivy download more comprehinsive vuln-list to scan the vulnearbitlies
- in large env you may set your own vuln list and trivy can use that list and scaning
- you can implement it in CICD envirnment as well.

## Tracee

- Tracee is tool to use, trace the system calls
- with UID,PID return code, and arguments
- you can narrow down with gpre
- this tool growing too fast, there could be new features

## Falco

- is open source tool
- passing linux system call from the kernel at runtime
- asserting the stream against a powerful rules engine
- alerting whe rule violated
- Falco is composed of three main components: a userspace program, configuration, and a driver.
- Falco some of tools are not backwards compatibilties
- If Sysdig updates their libraries, adding new fields checks and operators, Falco may not be able to interact with the library until an update is made available. As a result, the rules and the engine now support explicit versioning.
- you can configure the rules in falco with collection of key-value pairs
- rule
- description
- condition
- output
- priority
- Optionsl rules
- enabled | True:False
- Tags: run only those roles  filesystem, software_mgmt, process, database, host, shell, container, cis, users, network.
- warn_evttype: suppress warnings about a rule without an event type
- skip-if-unknown-filter:
