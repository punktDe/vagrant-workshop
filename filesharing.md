# File sharing between host and guest

## VirtualBox builtin file sharing

VirtualBox provides a [builtin capability](https://www.virtualbox.org/manual/UserManual.html#sharedfolders)
to share folders.

Unfortunately it is not supported for FreeBSD guests.

## NFS file sharing

The best we have for now is NFS. Unfortunately that leaves out Windows hosts.

### Requirements

Remember the host to guest network communication constraint concerning the NAT network?
So you must have a host-only network configured.

Vagrant will take care of sharing, mounting, unmounting - all automatically.

For that your local host user needs passwordless sudo privilege or you must enter a password
each time you `vagrant up`.

### Configuration

```ruby
  # share the project directory with the guest
  #
  config.vm.synced_folder '.', '/var/vagrant', :nfs => true, :nfs_version => 3
```

### Practical considerations

Vagrant does not create an `/etc/fstab` entry in the guest OS. Therefore each time
you reboot the guest OS from within the shared folder will not be present.

The mount is created dynamically at `vagrant up`.
