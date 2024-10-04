# AppArmor

- It's alternative (LSM) to SElinux
- support it has been incorporated in the linux kernel since 2006.

## AppArmor in Kubernetes

- in order apparmor use by pod, it must be on the node
- There is native process for kubernetes to load the policies. As result you need to ensure policies are loaded on every node where AppArmor-required pods are scheduled and scherl i sunaware of which node have profile.

## Modes and Profiles

- profile restrict how executable programs, which have pathnames on your system, such as /user/bin/evince, can be used. Process can run either of the following modes
- enforce: applications are prevented from activ in ways which are restricted.
- complain: it's learning mode, voilatin will be logged
