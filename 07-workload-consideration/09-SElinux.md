# SELinux overview

- Developed by US National Sec Admin
- SElinux is a set of security rules that are used to determine which processes can access which files, directories, ports and other items on the system.
- all objects are some sort of files and everything that is done is dome sort of process,
- SELinux can be used to control everything.
- SElinux works with these three conceptual quantities:
- Contexts: These are labels to files, processes and ports.
- rules: these describe access control in terms of contexts, processes, files, ports, users, etc
- Policies: They are set of rules that describe what system-wide access controle decision shoudl be made by SElinux
- SELinux context is a lablel used by a rule to define how users processes, files, and ports interact with each toerh.
- a default policy deny any access rules are used to describe allowed action on the sytem.
