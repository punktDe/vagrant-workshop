# vagrant-workshop

## Summary

Hashicorp Vagrant is a powerful platform for local automated creation and deployment of
virtual machines. This tutorial show the basics and two practical examples of how to use
Vagrant to create FreeBSD based development environments on a suitable machine.

Participants need an amd64 laptop and VirtualBox and Vagrant installed on their operating
system of choice to follow the practical parts of the tutorial. I'm using NFS for folder
sharing, so Windows is probably out. Mac OS, any BSD that supports VirtualBox, or Linux
will all do fine.

## Practical exercises

Some of the practical parts take the form of tasks to solve. For these in the `main`
branch the relevant parts of the Vagrantfiles are removed. Checkout the `solutions`
branch to see my suggested implementations.

## Agenda

* [Fundamentals](fundamentals.md)
* Managing [boxes](boxes.md)
* Practical: [bring up your first box](01_first_box/Vagrantfile)
* [Provisioners](provisioners.md)
* Practical: [install Apache to view the famous "It works!" page](02_apache/Vagrantfile)
* [Networking](networking.md) fundamentals
* Practical: [make Apache accessible from the host](03_host_access/Vagrantfile)
* More [networking](networking2.md)
* [File sharing](filesharing.md)
* Practical: [experiment with file sharing](04_filesharing/Vagrantfile)
* [Multiple VMs](multivm.md)
* Practical: [bring up three boxes in parallel](05_multivm/Vagrantfile)
* Practical: provision a Galera cluster
* How boxes are built
* Conclusion and questions
