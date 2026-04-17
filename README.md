# Networking-troubleshooting-lab-with-CISCO-Packet-tracer
Hands-on IT Support portfolio 

How to download Cisco packet tracer 

add the steps here later:






Day 1 — topic
Lab 1- Build a basic office network and assign IP addresses
Build a network with 1 router, 1 switch, and 2 PCs. Manually assign IPs. Ping PC1 from PC2 to confirm they can talk.

Packet tracer steps
Open Packet Tracer → drag 1 Router (2811), 1 Switch (2960), 2 PCs onto canvas
Connect PC0 → Switch with copper straight-through cable
Connect PC1 → Switch with copper straight-through cable
Connect Switch → Router Fa0/0 with copper straight-through cable
Click PC0 → Desktop → IP Configuration → set IP manually
Click PC1 → Desktop → IP Configuration → set IP manually
Click Router → CLI tab → configure the interface

IP address and subnetmask and default gateaway details:
-- On PC0: IP = 192.168.1.10 / Mask = 255.255.255.0 / Gateway = 192.168.1.1
-- On PC1: IP = 192.168.1.20 / Mask = 255.255.255.0 / Gateway = 192.168.1.1

-- Commands to type On Router CLI:
Router> enable
Router# configure terminal
Router(config)# interface FastEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit

-- Test from PC0 Desktop > Command Prompt:
ping 192.168.1.20

Issue you will see
Ping fails — "Request timed out" even after setting IPs correctly

Fix
The router interface is "administratively down" by default. You forgot no shutdown. Type it on the interface and ping again — it will work.

Lab: Basic office network
Issue: Ping failed between PC0 and PC1
Cause: Router interface was shutdown (administratively down)
Fix: Typed "no shutdown" on FastEthernet0/0
Verify: ping 192.168.1.20 — reply received
Save file as: lab01-basic-network.pkt


