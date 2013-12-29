vrrpd-startupscript
===================

Linux VRRPD startup script that supports multiple interface ( or VLANS )

Created under Ubuntu 12.04.3
Supports multiple interfaces.

Warning: Not tested on other distribution. sorry

Installation:
Copy all files to respective folders and across machines.

Configuring:
You rarely need to edit /etc/default/vrrpd

Add your interface configuration in /etc/vrrpd.d/$INTERFACE_NAME.conf

if your interface is eth0 then your configuration should be named: eth0.conf

if your NIC is on VLAN configuration, e.g.: eth0.152 for VLAN 152
your configuration file should be named : eth0.152.conf

the configuration is simple :
ID        is your VRRP ID, make sure you use same VRRPD ID accross same subnet
PRIORITY  is THIS server priority, higher priority will be the master
IP_ADDR   is the IP Address that would be switched for availability

Please see vrrpd documentation


