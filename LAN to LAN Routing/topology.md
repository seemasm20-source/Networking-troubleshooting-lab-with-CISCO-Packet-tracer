🖥️ Lab Topology









<img width="1920" height="1080" alt="Screenshot (204)" src="https://github.com/user-attachments/assets/e7285ed4-07ca-492e-b8c2-48b0f8855e6a" />



















⚙️ Step-by-Step Build Guide

🔧 Devices Used:


| DeviceModel       | Quantity | Purpose                       |
| ----------------- | :------: | ----------------------------- |
| Router Cisco 2911 | 1        | Routes traffic between 2 LANs |
| Switch Cisco 2960 | 2        | Connects PCs within each LAN  |
| PC Generic        | 6        | End user devices — 3 per LAN  |


⚙️ Step-by-Step Build Guide

   Step 1 — Add Devices to Canvas

1. Open Cisco Packet Tracer
  
2. Drag 1 x Router 2911    → place in the centre
 
3. Drag 2 x Switch 2960    → one left, one right of router
   
4. Drag 6 x PC             → 3 below each switch


Step 2 — Connect Cables

Use: Copper Straight-Through cable for all connections

PC1  FastEthernet0  →  Switch 1  any FastEthernet port

PC2  FastEthernet0  →  Switch 1  any FastEthernet port

PC3  FastEthernet0  →  Switch 1  any FastEthernet port

PC4  FastEthernet0  →  Switch 2  any FastEthernet port

PC5  FastEthernet0  →  Switch 2  any FastEthernet port

PC6  FastEthernet0  →  Switch 2  any FastEthernet port

Switch 1  GigabitEthernet  →  Router  GigabitEthernet0/0

Switch 2  GigabitEthernet  →  Router  GigabitEthernet0/1

✅ All cable dots turn green = connected correctly

🔴 Red dot = wrong cable or wrong port — delete and redo


Step 3 — Assign IPs to All PCs


For each PC:

Click PC → Desktop tab → IP Configuration → Static


| PC  | IP          | SubnetMask    | Default Gateway |
| --- | ----------- | ------------- | --------------- |
| PC1 | 10.0.0.1    | 255.255.255.0 | 10.0.0.4        |
| PC2 | 10.0.0.2    | 255.255.255.0 | 10.0.0.4        |
| PC3 | 10.0.0.3    | 255.255.255.0 | 10.0.0.4        |
| PC4 | 192.168.1.1 | 255.255.255.0 | 192.168.1.4     |
| PC5 | 192.168.1.2 | 255.255.255.0 | 192.168.1.4     |
| PC6 | 192.168.1.3 | 255.255.255.0 | 192.168.1.4     |



