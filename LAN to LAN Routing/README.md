LAN-to-LAN Routing Using Cisco Packet Tracer

IT Help Desk Tier 1 — Home Lab Portfolio Project 1
Tool: Cisco Packet Tracer
Author: [Seema]
Date: May14 2026


📌 Objective

This project models a network set-up consisting of two different departments HR(LAN1) and Finance(LAN2) working within two LAN-based networks. A Cisco router is used to enable interaction among the two departments while ensuring network segmentation.

The following are some of the basic networking principles covered in this project:

1.LAN segregation

2.IPv4 addressing

3.Routing configuration

4.Default gateway setting

5.Testing of connectivity

6.Network troubleshooting

🖥️ Network Topology

The network contains:

1. Cisco Router
2. Cisco Switches
3. 3 PCs in LAN1
4. 3 PCs in LAN2


🌐 Network Addressing Plan

| Department    | Network Address | Subnet Mask   | Gateway     |
| ------------- | --------------- | ------------- | ----------- |
| LAN1(HR)      | 10.0.0.1        | 255.255.255.0 | 10.0.0.4    |
| LAN2(Finance) | 192.168.1.1     | 255.255.255.0 | 192.168.1.4 |


🛠️ Technologies Used
1.Cisco Packet Tracer- Download 
2.Cisco Router
3.Cisco Switches
4.IPv4 Addressing
5.CLI Configuration
6.ICMP Ping Testing


⚙️ Configuration Tasks
  1.Router Configuration
  2.Assigned IP addresses to router interfaces
  3.Enabled interfaces using no shutdown
  4.Configured gateways for both LANs

 🖥️ PC Configuration
   1.Assigned static IP addresses
   2.Configured subnet masks
   3.Set default gateways


   🔍 Connectivity Testing

Connectivity between both LANs was verified using:
 ping command in command prompt
 ping 192.168.1.1
Note-Successful replies confirmed proper routing between the LAN1(HR) and LAN2(Finance) networks.

   
🧩 Troubleshooting Performed
1.Issue 1: PCs Could Not Communicate Across Networks
Cause
Incorrect default gateway configuration.

Solution
Configured the correct gateway addresses on all PCs.

Issue 2: Router Interface Down
Cause
Router interface was administratively disabled.

Solution
no shutdown command in Router command line interface


📚 Key Skills Demonstrated
 1.Inter-LAN Routing
 2.IPv4 Addressing
 3.Router CLI Configuration
 4.Network Troubleshooting
 5.Connectivity Verification

 📷 Screenshots

 Attached to the respective topics covered
 1.topology
 2.router configuration
 3.successful ping test
 4.troubleshooting 
 5. verification.


 🎯 Learning Outcome

This project provided hands-on experience with configuring LAN-to-LAN communication using Cisco devices in a simulated enterprise environment. It also strengthened troubleshooting and networking fundamentals relevant to IT Help Desk and IT Support roles.


✅ Conclusion

The project successfully established communication between two separate LAN networks using a Cisco router. This lab demonstrates foundational networking and troubleshooting skills commonly required in entry-level IT Support and Networking positions.
 


 
