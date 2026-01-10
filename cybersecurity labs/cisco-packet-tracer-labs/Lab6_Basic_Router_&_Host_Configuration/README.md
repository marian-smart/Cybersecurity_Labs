# Lab 6: Router Interface Configuration & End-Device Connectivity

## Objective
To configure a router hostname, assign IP addresses to router interfaces and PCs, verify interface status, and test end-to-end connectivity using ICMP pings.

## Devices Used
- Cisco Router (R1)
- Switch(es)
- PCs (PC1, PC2, PC3)

## Step-by-Step – What I Did

1. Opened Cisco Packet Tracer and accessed the router CLI.
2. Entered privileged EXEC mode and global configuration mode.
3. Configured the router hostname.

enable
configure terminal
hostname R1

4. Used a show command to view available interfaces, IP addresses, and interface status.

show ip interface brief

5. Configured IP addresses on R1’s interfaces and enabled them.
   Also added interface descriptions for clarity.

interface g0/0
description Connection to LAN 1
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

interface g0/1
description Connection to LAN 2
ip address 192.168.2.1 255.255.255.0
no shutdown
exit

6. Verified interface configuration and status.

show ip interface brief

7. Viewed the running configuration to confirm all changes.

show running-config

8. Saved the running configuration to startup configuration.

copy running-config startup-config

9. Configured IP addresses on PC1, PC2, and PC3 using the Desktop > IP Configuration menu in Packet Tracer.

   - Assigned IP address
   - Assigned subnet mask
   - Configured default gateway pointing to R1

10. Tested network connectivity by pinging between PCs.

ping 192.168.1.2
ping 192.168.2.2

## Result
- Router hostname was successfully configured.
- Router interfaces were assigned IP addresses and enabled.
- PCs were correctly configured with static IP addresses.
- Successful ping tests confirmed end-to-end connectivity.
- Configuration was saved and verified.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI
- ICMP (Ping)

