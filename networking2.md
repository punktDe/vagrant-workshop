# Networking constraints in VirtualBox

Again, refer to the [VirtualBox networking documentation](https://www.virtualbox.org/manual/UserManual.html#networkingdetails)
for details.

## IP address ranges for the host-only network(s)

On Linux, macOS and Solaris VirtualBox will only allow IP addresses in the
`192.168.56.0/21` range to be assigned to host-only adapters. For IPv6 only
link-local addresses are allowed.

To change that create the file `/etc/vbox/networks.conf` and place something like
this in there:

```sh
* 10.0.0.0/8 192.168.0.0/16
* 2001::/64
```

or

```sh
* 0.0.0.0/0 ::/0      
```
