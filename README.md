LAN-to-LAN Routing Using Cisco Router

IT Help Desk Tier 1 Portfolio Project
Built and documented by: SEEMA S M
Tool: Cisco Packet Tracer
Date: April 2026

How to download Cisco packet tracer : https://www.netacad.com/courses/getting-started-cisco-packet-tracer?courseLang=en-US
1. go to browser and find NETACAD.com
2. Sign up to the account as a new user
3. Give required details like Name, email address,dob
4. tick off all terms and condition of cisco networking
5. next it navigates to explore the catalog page
6. getting started with cisco packe tracer
7. Install cpt
8. download the version of packet tracer
9. choose the machine you want to work with 9.00.0 for Windows 64 bit
10. download the exe file and click on downloaded file ( snapshots attached for next steps)


[Cisco_Packet_Tracer_Download_and_Installation_Instructions.pdf](https://github.com/user-attachments/files/27069556/Cisco_Packet_Tracer_Download_and_Installation_Instructions.pdf)



Objective:
🔧Connect two separate LAN networks using a single Cisco 2911 router and enable full communication between all PCs across both networks(using Cisco Packet Tracer)


1. Network Topology
 
🔧 Devices Used
     Device                        Model                Quantity                Purpose 
     Router Cisco                       Cisco 2911             1                     Routes traffic between 2 LANs
     Switch                             Cisco 2960             2                     Connects PCs within each LAN
     PC                                 Generic PC             6                     End user devices (3 per LAN)

2. 📋 IP Address Table
   
    Device        Interface                 IPAddress                   SubnetMask          Default Gateway
   
   Router         GigabitEthernet0/0        10.0.0.4                    255.255.255.0        _
   
   Router          GigabitEthernet0/1       192.168.1.4                 255.255.255.0        _

   PC1 (LAN 1)     FastEthernet0            10.0.0.1                     255.255.255.0      10.0.0.4

   PC2(LAN 2)      FastEthernet0            10.0.0.2                     255.255.255.0      10.0.0.4

   PC3(LAN 3)      FastEthernet0             10.0.0.3                    255.255.255.0       10.0.0.4

   PC4(LAN 4)      FastEthernet0             192.168.1.1                  255.255.255.0       192.168.1.4

   PC5(LAN 5)      FastEthernet0              192.168.1.2                  255.255.255.0       192.168.1.4

   PC6(LAN 6)      FastEthernt0               192.168.1.3                   255.255.255.0       192.168.1.4

   
3. Packet tracer steps
   Build a network with 1 router, 2 switch, and 3 PCc in each network:
   
   a.Open Packet Tracer → drag 1 Router (2911), 1 Switch (2960), 3 PCs onto canvas.
   b. Connect PC1 → Switch with FastEthernet cable
   c. Connect PC2 → Switch with FastEthernet cable
   d. Connect PC3 → Switch with FastEthernet cable
   e. Connect Switch → Router GigabitEthernet0/0 with copper straight-through cable

    a. Open Packet Tracer → drag 1 Router (2911), 1 Switch (2960), 3 PCs onto canvas.
    b. Connect PC4 → Switch with FastEthernet cable
    c. Connect PC5 → Switch with FastEthernet cable
    d. Connect PC6 → Switch with FastEthernet cable
    e. Connect Switch → Router GigabitEthernet0/1 with copper straight-through cable
      
  4.  Manually Assign IP address to all the PCS starts from PC1 TO PC6.
     a. Click PC1 → Desktop → IP Configuration → set IP manually
     b. Click PC2 → Desktop → IP Configuration → set IP manually
     c. Click PC3 → Desktop → IP Configuration → set IP manually
     d. Click PC4 → Desktop → IP Configuration → set IP manually
     e. Click PC5 → Desktop → IP Configuration → set IP manually
     f. Click PC6 → Desktop → IP Configuration → set IP manually

 5. Click Router → Config tab → Select the Interface → GigabitEthernet0/0 → Click on CLI tab → configure the interface
    Commands to type On Router CLI:

    Router> enable

    Router# configure terminal

    Router(config)# interface GigabitEthernet0/0

    Router(config-if)# ip address 10.0.0.4 255.255.255.0

    Router(config-if)#  shutdown

    Router(config-if)# exit
    

    Router> enable

    Router# configure terminal

    Router(config)# interface GigabitEthernet0/1

    Router(config-if)# ip address 192.168.1.4 255.255.255.0

    Router(config-if)#  shutdown

    Router(config-if)# exit

    

6. Issues : 1
 a. Test from PC1 Desktop > Command Prompt
 b. ipconfig
 c.ping PC1 to PC3 ( PC1 ip address-10.0.0.1 , PC3 ip address- 192.168.1.1
 d. Ping 192.168.1.1 in command prompt
 e. Ping fails — "Request timed out" even after setting IPs correctly

<img width="1920" height="1080" alt="Screenshot (215)" src="https://github.com/user-attachments/assets/6ef852a6-211b-49de-ad42-06c6582d7adf" />
<img width="1920" height="1080" alt="Screenshot (214)" src="https://github.com/user-attachments/assets/4ac121eb-603f-4b70-aa5b-94f87fe92ff4" />






   7. Fix :
   a. Default gateway was not assigned to the PCs.
   b. Default gateway will be Routers IP address
   c. IP address and subnetmask and default gateaway details:
       On PC1: IP = 10.0.0.1 / Mask = 255.255.255.0 / Gateway = 10.0.0.4
          PC2: IP = 10.0.0.2 / Mask = 255.255.255.0 / Gateway = 10.0.0.4
          PC3: IP = 10.0.0.3 / Mask = 255.255.255.0 / Gateway = 10.0.0.4
      On PC4: IP = 192.168.1.1 / Mask = 255.255.255.0 / Gateway = 192.168.1.4
         PC5: IP = 192.168.1.2 / Mask = 255.255.255.0 / Gateway = 192.168.1.4
         PC6: IP = 192.168.1.3 / Mask = 255.255.255.0 / Gateway = 192.168.1.4
      d. Click PC1 → Desktop → IP Configuration → set Default Gateway to all the PCs.
      e.  Assigned Default Gateaway and PCs started communicating to each other.

<img width="1920" height="1080" alt="Screenshot (221)" src="https://github.com/user-attachments/assets/2b609d9f-657e-417f-8a65-95f461bde0fe" />
<img width="1920" height="1080" alt="Screenshot (220)" src="https://github.com/user-attachments/assets/cfbe8ba0-2ee2-4be0-8c45-4422441c0bdd" />
<img width="1920" height="1080" alt="Screenshot (219)" src="https://github.com/user-attachments/assets/f43e7209-5983-4aac-af47-74a5a9ce9bf2" />
<img width="1920" height="1080" alt="Screenshot (218)" src="https://github.com/user-attachments/assets/113df17a-7370-47e9-bf9f-4f8e5369793a" />
<img width="1920" height="1080" alt="Screenshot (217)" src="https://github.com/user-attachments/assets/5317f79b-8d41-414d-9666-66e4acfc680e" />
<img width="1920" height="1080" alt="Screenshot (216)" src="https://github.com/user-attachments/assets/c791e471-0062-44be-b637-c2f03d9bd26d" />

   



Issues -2

8. Issue: Ping failed between PC0 and PC1
   Cause: Router interface was shutdown (administratively down)




















<img width="1920" height="1080" alt="Screenshot (228)" src="https://github.com/user-attachments/assets/177fff40-c92b-4d2e-9552-3cb21791bcd7" />
<img width="1920" height="1080" alt="Screenshot (227)" src="https://github.com/user-attachments/assets/745a42a5-3d61-495d-9bb0-3f67d0bb5685" />
<img width="1920" height="1080" alt="Screenshot (226)" src="https://github.com/user-attachments/assets/6fbdb454-b545-4379-be5f-9a97b3e372cb" />
<img width="1920" height="1080" alt="Screenshot (225)" src="https://github.com/user-attachments/assets/03eff9b8-ef29-4756-ad98-de311c060100" />
<img width="1920" height="1080" alt="Screenshot (224)" src="https://github.com/user-attachments/assets/1b21a299-a2fc-4b18-921a-004639aa3098" />





-- Test from PC0 Desktop > Command Prompt:

ping 192.168.1.20

Issue you will see


Ping fails — "Request timed out" even after setting IPs correctly
     
Fix

The router interface is "   m      dministratively down" by default. 

You forgot no shutdown. Type it on the interface and ping again — it will work.

Lab: Basic office network

Issue: Ping failed between PC0 and PC1

Cause: Router interface was shutdown (administratively down)

Fix: Typed "no shutdown" on FastEthernet0/0

Verify: ping 192.168.1.20 — reply received

Save file as: lab01-basic-network.pkt


