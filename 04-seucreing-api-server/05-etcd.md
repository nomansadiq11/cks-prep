# ETCD db


## Persistent State from etcd

- Must protect the etcd database, this only contains everything about cluster, like secretes and configmap.
- if this is compromised your pods results will be different.
- only the api-server communcate with etcd and you should allow only TLS.


## Encryption data at rest

- encryt the data at rest
- instead of base64 encryption, you should configure custome configuration
- keep the old encryption key same file like 2nd line for older secretes to read

### Encryption Providers

- Identity
- aescbc
- secretbox
- aesgcm
- kms


Note:
- In encryption policy file you can mentioned which resouces you want to encrypt.
-  All the following keys would be kept in case you want to read a previously encrypted resource. If you delete the old keys prior to rewriting the resource, you will not be able to access those resources again.
