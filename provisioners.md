# Provisioners

A [provisioner](https://developer.hashicorp.com/vagrant/docs/provisioning) specifies
the code to be run on initial `vagrant up` or subsequently on `vagrant provision`.

It implements all customisations of your box you want to take place
automatically and reproducably ("infrastructure as code").

You can have multiple provisioners in your Vagrantfile.

## File

The `file` provisioner copies a file from your local directory to some location
inside the VM.

## Shell

The simplest provisioner that actually runs code is the `shell` provisioner.

### Inline

```ruby
  config.vm.provision 'shell', inline: <<-SHELL
    # here go your shell commands
  SHELL
```

### External script

```ruby
  config.vm.provision "shell", path: "script.sh"
```

## Ansible

You can run an [Ansible play](https://developer.hashicorp.com/vagrant/docs/provisioning/ansible_intro)
either locally on your host or inside the virtual machine. Our most frequent approach is
to run Ansible on the host executing the configuration tasks inside the VM.

## Others

[There are a ton more](https://developer.hashicorp.com/vagrant/docs/provisioning).
Check if your favourite config management tool is supported.
