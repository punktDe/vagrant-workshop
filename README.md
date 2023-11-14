# vagrant-workshop

## Summary

Hashicorp Vagrant is a powerful platform for local automated creation and deployment of
virtual machines. This tutorial shows the basics and practical examples of how to use
Vagrant to create FreeBSD based development environments on a suitable machine.

Participants need an amd64 laptop and VirtualBox and Vagrant installed on their operating
system of choice to follow the practical parts of the tutorial. I'm using NFS for folder
sharing, so Windows is probably out. Mac OS, any BSD that supports VirtualBox, or Linux
will all do fine.

## Agenda

* [Fundamentals](fundamentals.md)
* Managing [boxes](boxes.md)
* Practical 1: [bring up your first box](01_first_box/Vagrantfile)
* [Provisioners](provisioners.md)
* Practical 2: [install Apache to view the famous "It works!" page](02_apache/Vagrantfile)
* [Networking](networking.md) fundamentals
* Practical 3: [make Apache accessible from the host](03_host_access/Vagrantfile)
* More [networking](networking2.md)
* [File sharing](filesharing.md)
* Practical 4: [experiment with file sharing](04_filesharing/Vagrantfile)
* [Multiple VMs](multivm.md)
* Practical 5: [bring up three boxes in parallel](05_multivm/Vagrantfile)
* [Ansible integration](ansible.md)
* Practical 6: [deploy a distributed application with Ansible](06_ansible/Vagrantfile)
* [How boxes are built](boxbuilding.md)

## Related projects:

* [Vagrant OPNsense](https://github.com/punktDe/vagrant-opnsense) - run an OPNsense firewall on your desktop for development
* [Vagrant FreeBSD Boxbuilder](https://github.com/punktDe/vagrant-freebsd-boxbuilder) - automatically build boxes
