# homelab-k8s-ha-cluster_components-etcd
Playbook that deploys a HTTP etcd cluster. See branch https_modification for the HTTPS, TLS enabled version of the cluster.

# Sanity Check

The following commands are to be ran to check for sanity.

To check cluster health, on a random etcd node, run:

```
etcdctl endpoint health --cluster
```

on etcd node 1 run:

```
etcdctl put foo "bar"
```

on etcd node 2 run:

```
etcdctl get foo
```
