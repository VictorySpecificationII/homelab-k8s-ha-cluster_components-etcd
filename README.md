# homelab-k8s-ha-cluster_components-etcd
Playbook that deploys a HTTPS, TLS enabled etcd cluster with self-signed certificates.

# Sanity Check

The following commands are to be ran to check for sanity.

To check cluster health, on a random etcd node, run:

```
etcdctl --cacert /etc/etcd/ssl/ca.crt endpoint health --cluster
```

on etcd node 1 run:

```
etcdctl --cacert /etc/etcd/ssl/ca.crt put foo "bar"
```

onn etcd node 2 run:

```
etcdctl --cacert /etc/etcd/ssl/ca.crt get foo
```
