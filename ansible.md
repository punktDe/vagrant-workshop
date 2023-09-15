# Ansible integration

## Considerations

Ansible provisioner for Vagrant exists, but we prefer to use a virtual environment.

So we do that and specify e.g. `vagrant` as the remote user and the Vagrant generated
SSH key files for authentication.

If you run `ssh-agent` with lots of keys preloaded, you need to add `-o IdentitiesOnly=yes`
to your `ssh` default parameters. All of this can be set in `ansible.cfg`

## Getting fancy

Beyond the scope of this particular tutorial, but you can build either the list of
VMs to provision in Vagrant from the Ansible inventory or vice versa! Pick what
suits you best.

As a last practical exercise we will use a small Ansible project to deploy a clustered
application.
