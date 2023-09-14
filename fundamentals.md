# Fundamentals

## Boxes

Boxes are what Vagrant manages for you. A box is an instance of a virtual machine
cloned from a repository of template boxes.

Template boxes can be automatically downloaded from a repo similar to Docker Hub
or manually imported from a file.

You can also create your own.

The public repo provided by Hashicorp is at https://app.vagrantup.com/

To import the box for this tutorial from a file use

```sh
vagrant box add freebsd-132-ufs.box --name punktde/freebsd-132-ufs
```

## Providers

A provider is a hypervisor providing the environment to run your VM. Providers
are among others

* VirtualBox
* libvirt/KVM
* Vmware Workstation/Fusion
* ...

The most common provider for development on a desktop machine is probably VirtualBox.

There is an [ongoing effort](https://forums.virtualbox.org/viewtopic.php?t=107344) to make Intel/AMD64 virtual machines run in VirtualBox on
an Apple Silicon Mac.

## Vagrantfile

The [Vagrantfile](https://developer.hashicorp.com/vagrant/docs/vagrantfile) is a high level description of your Vagrant project, the box(es) used and their particular configuration.

It's essentially Ruby turned into DSL.

## SSH keys

Vagrant uses a fixed not-so-private SSH key to login to the VM at first startup.
The key is then replaced with a dynamically generated one specific to the particular
project.

## File locations

The state, specific settings, and most important the SSH private key for a project are
stored in `<project directory>/.vagrant`.
Template boxes, plugins, global settings are stored in `~/.vagrant.d`.
