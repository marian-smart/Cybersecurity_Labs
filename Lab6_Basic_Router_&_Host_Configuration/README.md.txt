# Lab 4: Router Interface Configuration & End-Device Connectivity

## Objective
To configure a router hostname, assign IP addresses to router interfaces and PCs, verify interface status, and test end-to-end connectivity using ICMP pings.

## Devices Used
- Cisco Router (R1)
- Switch(es)
- PCs (PC1, PC2, PC3)

## Step-by-Step – What I Did

1. Opened Cisco Packet Tracer and accessed the router CLI.
2. Entered privileged EXEC mode and global configuration mode.
3. Configured the router hostname using the commands:

enable
configure terminal
hostname R1

4. Used a show command to view available interfaces, IP addresses, and interface status using the command:

show ip interface brief

5. Configured IP addresses on R1’s interfaces and enabled them, and also added interface descriptions for clarity using the commands:

interface g0/0
ip address 15.255.255.254 255.0.0.0
description ## to SW1 ##
no shutdown

interface g0/1
ip address 182.98.255.254 255.255.0.0
description ## to SW2 ##
no shutdown

interface g0/2
ip address 201.191.20.254 255.255.255.0
description ## to SW3 ##
no shutdown

6. Verified interface configuration and status using the command:

show ip interface brief

7. Viewed the running configuration to confirm all changes  using the command:

show running-config

8. Saved the running configuration to startup configuration using the command:

copy running-config startup-config

9. Configured IP addresses on PC1, PC2, and PC3 using the Desktop > IP Configuration menu in Packet Tracer.

   - Assigned IP address
   - Assigned subnet mask
   - Configured default gateway pointing to R1

10. Tested network connectivity by pinging between PCs using the commands:

ping 182.98.255.254
ping 201.191.20.254

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

