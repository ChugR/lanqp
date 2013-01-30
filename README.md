lanqp
=====

To create a network interface called 'lanq0' with an address of 10.1.1.1/16:

$ sudo tunctl -t lanq0 -n -u _your-user-id_
$ sudo ifconfig lanq0 10.1.1.1 netmask 255.255.0.0 up

You will need to have a nexus-router process running in a location that is reachable from all
lanqp instances.

To run lanqp:

$ ./lanqp _host-of-router_ _port-of-router_ lanq0 _vlan-name_ _ip-of-lanq0_

example:

$ ./lanqp router-host 5672 lanq0 my-vlan 10.1.1.1

