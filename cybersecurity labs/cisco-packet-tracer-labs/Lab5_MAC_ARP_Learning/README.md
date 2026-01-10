# Lab 4: MAC Address Learning and ARP Behavior

## Objective
To observe how switches learn MAC addresses and how ARP and ICMP traffic work when devices communicate on a network with empty MAC and ARP tables.

## Initial Network State
- Both switches had empty MAC address tables
- All PCs had empty ARP tables

## Devices Used
- Switches
- PCs

## Step-by-Step – What I Did

### 1. Initial Ping from PC1 to PC3
1. I ensured all switches had empty MAC address tables.
2. I ensured all PCs had empty ARP tables.
3. From **PC1**, I sent a ping to **PC3**.

### What Happened on the Network
- PC1 did not know PC3’s MAC address.
- PC1 sent an **ARP Request (broadcast)**.
- Both switches flooded the ARP request to all connected devices.
- PC3 received the ARP request and replied with an **ARP Reply (unicast)**.
- The switches learned the MAC addresses of PC1 and PC3.
- After ARP resolution, **ICMP Echo Request and Echo Reply** packets were exchanged.

---

### 2. Verification Using Simulation Mode
1. I switched Packet Tracer to **Simulation Mode**.
2. I replayed the ping.
3. I observed:
   - ARP Request (broadcast)
   - ARP Reply (unicast)
   - ICMP Echo Request
   - ICMP Echo Reply
4. I inspected packet details to confirm Layer 2 and Layer 3 operations.

---

### 3. Generating Traffic for MAC Learning
1. I sent pings between all PCs.
2. This generated enough traffic for the switches to learn the MAC addresses of every connected PC.

---

### 4. Viewing MAC Address Tables
1. On each switch, I opened the CLI.
2. I ran the command:
```bash
show mac address-table
3. I identified which MAC address belonged to each PC and the switch port it was learned on.

### 5. Clearing Dynamic MAC Addresses

1. On each switch, I cleared learned MAC addresses using:
```bash
clear mac address-table dynamic
2. I confirmed that the MAC address tables were empty again.

### Result

- Observed ARP broadcast and unicast behavior.

- Switches dynamically learned MAC addresses from network traffic.

- Verified MAC-to-port mappings using show commands.

- Successfully cleared dynamic MAC entries.

### Tools Used

- Cisco Packet Tracer

- Simulation Mode

- Switch CLI
