# OpenWRT Virtual Machine Setup

<br>

`OpenWrt` acts as the lab’s virtual router and network gateway. It provides routing, firewall control, DHCP services, and traffic separation between the server and workstation subnets, helping the environment behave more like a real small enterprise network.

<br>

#### VMware Workstation Settings

To prepare the environment for OpenWrt, I first configured VMware’s virtual networks to act as the backbone of the lab. These networks allow the router, servers, and workstations to communicate while keeping each subnet properly separated.


<br>

#### Preparing OpenWRT ISO

By default, OpenWRT is downloaded as a .img file since it meant to be flashed onto network hardware.
Since VMware Workstation does not natively support .img files, I needed to convert it to a vmdk file.

After some research, I decided to using `qemu-tools` in WSL in order to complete the conversion.


```bash

hello

```
