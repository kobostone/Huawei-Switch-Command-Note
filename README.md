# Huawei-Switch-Command-Note
Huawei Switch Configuration short note

Contains Configuration commands: VLAN

### Interface Configuration ⚙️

-  <HUAWEI> display ip interface brief # switch IP address
   <HUAWEI> display interface brief 


### Giving the switch an IP address

- system-view    
- interface Vlanif 1   
- ip address 10.1.1.1 30
- display this    
- quit     
<Huawei>display ip interface brief	


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


## Verify VLAN Configuration   

[switch1]display vlan summary	      
[switch1]display vlan	     
[switch1]display vlan 10	Show all information of vlan 10     
[switch1]display port vlan	To view types of port and VLAN configuration    

## Find out the connected devices to a Huawei switch 

#view the LLDP neighbors of the switch. This will show you information about neighboring devices that support the LLDP protocol,

display lldp neighbor    
display lldp neighbor brief      
display lldp neighbor interface XGigabitEthernet 2/2/4   

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


