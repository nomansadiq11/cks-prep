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

## SELinux Enforcement Modes

- SElnux mode are selected in a file usually location /etc/selinux/config or depends on various distribution

### Enforcing

- All SELinux code is operative and access is denied according to the policy.
- all audit violation are logged
- there are many violation which are not logged, some various has ten thours message which are not logged.
- they are part of dontaudit list

### Permissive

- Enable SELinux code, but only warns about operations that would have been denied in enforcing mode.
- The dontaudit log remain slient

### Disabled

- you can disabled the SELinux kernael and application code leaving the system without any its protections.
- the only way to enter or leave this mode is to reboot.
- if you eanble again you should configure longer boot time
- there are utitlize to see the status
- getenforce and setenfor to see or set the current mode

### getenforce and setenforce

- you can get the SELinx info by using getenforce
- setenforce you can swtich between permissive and enforce modes
- if you need to disable it you need to update on the config file in SELinux

### SELinux Policy

- Same config file use for configure the policy
- configuring the policy need reboot which is time consuming process
- multiple policies are allowed only one policy will be active

### Context Utilities

- context are lables
- lables are applied to files, ports, processes and directories
- There are four SELinux contexts : User, Role, Type, and level
- using context utility we can change the context and view the context

### SELinux and Standard commands

- many standard command extend support for SELinux
- like ls and usually add Z with it will show the labels

### Context Inheritance

- newly created files interit the context from partent directory
- cpying and moving the files, context source directory will retain, this can cause the issue
- using command restorecon can reset the context in the directory, which will interit the context from parent directory.
- semanage chagne the default context but not the existing files context

### using SELinux Booleans

- A boolean value either true of false
- you can change teh default functionality without reading the code
- like you can disable allow_ftpd_anon_write boolean may allow serval process to act on files, otherwise disallowed

### monitoring SELinux access

- The settroulbeshoot server package provides tools to collect issues at runtime, log them and propose solutions to prevent the issue in the future.
- after installation of the package, auditd to restart. raw error will be tagged as AVC errors and appended to the audit.log
- more human readable errors will logged in /var/log/messages
