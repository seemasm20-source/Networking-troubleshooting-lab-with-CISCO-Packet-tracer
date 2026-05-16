 Configuration of  Router via Command line interface:
 










<img width="1920" height="1080" alt="Screenshot (224)" src="https://github.com/user-attachments/assets/b43cb749-69aa-4230-a631-4033c7c743dd" />









 Click Router → CLI tab → press Enter to begin

Router> enable

Router# configure terminal

! --- LAN 1 interface ---

Router(config)# interface GigabitEthernet0/0

Router(config-if)# ip address 10.0.0.4 255.255.255.0

Router(config-if)# no shutdown

Router(config-if)# exit

! --- LAN 2 interface ---

Router(config)# interface GigabitEthernet0/1

Router(config-if)# ip address 192.168.1.4 255.255.255.0

Router(config-if)# no shutdown

Router(config-if)# exit


! --- Save configuration ---
Router# write memory






Note: The Default Gateway on every PC is the router's IP address on that PC's side.



LAN 1 PCs use 10.0.0.4 and LAN 2 PCs use 192.168.1.4
