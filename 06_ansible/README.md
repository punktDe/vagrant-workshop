# Using Ansible to configure a Vagrant provisioned cluster

## Installing and/or activating the virtual environment

```sh
source .envrc
````

## Run Ansible to execute a command on every node

```sh
ansible -m shell -a "freebsd-version" all
```

## Run Ansible play to install Redis Ron all nodes

```sh
ansible-playbook pb_redis.yml
```

Redis will be set up with `node1` as the replication leader and
`node2` and `node3` as followers. Success can be verified by looking
at `/var/log/redis/redislog` on the nodes.

The nodes can communicate freely via the host-only network.
