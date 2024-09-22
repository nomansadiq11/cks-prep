# Calico

- Calico support kubernetes NetworkPolicy object
- it's support IPVS but require some configuration
- its also has own policies which seamless for kubernets
- The use of GlobalNetworkPolicy spans all the namespaces. This take precedence over other configurations such as profiles.
- Calico network plugin can also be use for eBPF data plane, which replace ip table functionaly and number of performance incesses
