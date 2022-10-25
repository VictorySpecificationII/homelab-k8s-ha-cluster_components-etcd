# homelab-k8s-ha-cluster_components-etcd
Playbook that deploys a HTTPS etcd cluster.

# Sanity Check

The following commands are to be ran to check for sanity.

To check cluster health run:

```
etcdctl --cacert /etc/etcd/ssl/ca.crt endpoint health --cluster

on etcd node 1 run:

```
etcdctl --cacert /etc/etcd/ssl/ca.crt put foo "bar"

onn etcd node 2 run:

```
etcdctl --cacert /etc/etcd/ssl/ca.crt get foo

