# Networking fundamentals

[VirtualBox networking](https://www.virtualbox.org/manual/UserManual.html#networkingdetails)
while porwerful comes with its own set of assumptions and constraints.

## NAT network

Every VM has got at least a NAT network adapter. VirtualBox provides DHCP, default gateway
and recursive DNS to the VM(s), then NAT's this network outbound to the host's network
connection.

In the Vagrant context we will use the NAT network for the VM to access the Internet.

*Unless explicit port forward setups are configured the host cannot communicate with
the VM via the NAT network. This is different from e.g. VMware Fusion.*

A port forward for SSH is configured by default. This is what `vagrant ssh` uses.

## Bridged network

You can configure a bridged configuration using your host's connection. The VMs will
have access to the physical wired or wireless network that your host is connected to.
Especially in a wired environment you can make full use of your local infrastructure
that way.

## Host-only network

A host-only network is a virtual switch that your host and your VMs plug into.
The host and the VMs can all communicate with each other. We will use host-only
networks to build our virtual infrastructure.
