# Multiple VMs

Multiple VMs can be brought up as easily as a single one. Vagrant can
apply common default settings and provisioners while at the same time
overriding single things per VM.

You have the full power of Ruby at your hand for scripting, e.g.

* read an Ansible or Chef inventory
* build a list of VMs and settings from that
* loop over the list and configure and provision the machines

## Example

See in the [next practical part](05_multivm/Vagrantfile).

## Start/stop the VMs

```sh
vagrant up --parallel
vagrant halt --parallel
 ```

## Manage individual VMs

```sh
vagrant up <vm>
vagrant halt <vm>
vagrant provision <vm>
vagrant ssh <vm>
vagrant ssh <vm> -c "<command>"
```
