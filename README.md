# Huawei-Switch-Command-Note
Huawei Switch Configuration short note


![image](https://github.com/user-attachments/assets/88840a90-7369-443f-91fc-facde9774d63)



### Display Interface Configuration ⚙️

-  <HUAWEI> display ip interface brief     
   <HUAWEI> display interface brief 


### Giving the switch an IP address

<HUAWEI> system-view
[HUAWEI] 
   
  
![image](https://github.com/user-attachments/assets/17ea9407-2604-4627-a626-9fa6f7a06570)



  ## Verify VLAN Configuration   

- system-view  
[switch1]display vlan summary	      
[switch1]display vlan	     
[switch1]display vlan 10	   Show all information of vlan 10     
[switch1]display port vlan	   view types of port and VLAN configuration    

![image](https://github.com/user-attachments/assets/970cefb1-f2f7-4de6-af3c-0412324f42e6)

![image](https://github.com/user-attachments/assets/3779a87a-ff9e-4010-9b2d-c7460b9fbfc4)


### View VLAN ⚙️   

- system-view   
- display vlan
- 
### Assign an access Interface to VLAN ⚙️   

Assign interface GigabitEthernet 0/0/2 to Vlan 10

[switch1]`interface GigabitEthernet 0/0/2`      
[switch1-GigabitEthernet0/0/2]`port link-type access`       
[switch1-GigabitEthernet0/0/2]`port default vlan 10`       
[switch1-GigabitEthernet0/0/2]quit


### Configuring a trunk interface ⚙️ 

Assign interface GigabitEthernet 0/0/4 as a trunk interface:   

[switch1]`interface GigabitEthernet 0/0/4`   
[switch1-GigabitEthernet0/0/4]`port link-type trunk`    
[switch1-GigabitEthernet0/0/4]`port trunk allow-pass vlan 10 , 20`   •	Allow specific VLANS to this interface
[switch1-GigabitEthernet0/0/4]port trunk allow-pass vlan all    
[switch1-GigabitEthernet0/0/4]`port trunk pvid vlan 10`    •	Set default VLAN for trunk interface.
[switch1-GigabitEthernet0/0/4]quit

![image](https://github.com/user-attachments/assets/437be43d-e9bc-48a3-861d-4e51e4cfb4f5)



## Find out the connected devices to a Huawei switch 

#view the LLDP neighbors of the switch. This will show you information about neighboring devices that support the LLDP protocol

display lldp neighbor    
display lldp neighbor brief      
display lldp neighbor interface XGigabitEthernet 2/2/4   

[HUAWEI] display lldp local interface Gigabitethernet 0/0/1
Error: The LLDP is not enabled on this port.
<HUAWEI> system-view
[HUAWEI] lldp enable

<HUAWEI> system-view
[HUAWEI] interface gigabitethernet 0/0/1
[Quidway-GigabitEthernet1/0/1] lldp enable
Info: The LLDP is enabled on the port successfully.

and     
 "display mac-address"    
 "display arp"      
 "display interface brief"    
 

 
 
These commands will provide you with information about the MAC addresses, IP addresses, interfaces, and neighboring devices 
connected to the switch.

## Find out a mac address

searching for iMAC address "0011-2233-4455":    
display mac-address 0011-2233-4455     

For example, to search for MAC addresses on interface GigabitEthernet 0/1/1,    
display mac-address GigabitEthernet 0/1/1     

You can also search for MAC addresses associated with a specific VLAN.    
display mac-address vlan 10    
display mac-address vlan 4 GigabitEthernet 0/1/1    


![image](https://github.com/user-attachments/assets/810b73d1-386e-469f-a25b-1459ea29205c)

![image](https://github.com/user-attachments/assets/8651914c-6bd5-459e-9cce-11ceac1b9782)

![image](https://github.com/user-attachments/assets/780c58d4-3f06-4954-9e48-d935eb77bafe)


![image](https://github.com/user-attachments/assets/966f4f86-0529-401b-8553-b9d0ef8ac389)


![image](https://github.com/user-attachments/assets/09f8e033-a00d-4856-9249-d23a3dfbf4e2)

