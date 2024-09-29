# Leverage Admission Controller

- There are serveral place you can do static and dynamic analysis
- before depoyment to prod envirement runs on cicd processes
- one more way you can leverage the admision controller to scan and approve image
- but this will take time to download the image and scan it everytime new container will create
- A common option is to leverage a dynamic admission controller to insert an initContainer: containing a scan or verification tool into the pod spec. Then the load is distributed across all the workers. Only if the initContainer: scans and has a zero exit code, is the rest of the pod spec passed to the container engine for execution. This is the way that TrendMicro offers some of their cloud security tools.
