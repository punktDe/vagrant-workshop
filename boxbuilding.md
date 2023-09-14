# Where do baby boxes come from?

You can turn a manually configured VirtualBox VM into a Vagrant box.

Most importantly you need to create a user with

* the name `vagrant`
* the not-so-secret public key for SSH login
* passwordless `sudo``

For fully automatic creation of customised FreeBSD boxes from existing
FreeBSD boxes you might want to look at this project:

[Vagrant FreeBSD Boxbuilder](https://github.com/punktDe/vagrant-freebsd-boxbuilder)
