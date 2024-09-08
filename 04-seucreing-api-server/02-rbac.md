# Role Based Access Control

- The use of RBAC has been enabled by default since v1.6. As all resources are modeled API objects, they can be modified via Create, Read, Update, Delete (CRUD) operations. These are operations such as create, get, update, edit, watch and exec, among others. Allowed operations are defined in the serverresources.json file per object.

## role vs clusterrole

- role created for only specfic namespace
- clusterrole created for whole cluster

## rolebinding vs clusterrolebinding

- rolebinding same like only for specfic namespace
- clusterrolebinding for whole cluster 
