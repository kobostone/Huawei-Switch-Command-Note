# Huawei-Switch-Command-Note


### Display Interface Configuration ⚙️

-  <HUAWEI> display ip interface brief     
   <HUAWEI> display interface brief

   
![image](https://github.com/user-attachments/assets/97882078-bf35-4335-971d-7670b25fbbf0)


![image](https://github.com/user-attachments/assets/1193ba10-54da-4f0f-b856-e250230c3024)

![image](https://github.com/user-attachments/assets/002dbe7f-8579-4af1-b3d2-21a8065cc59c)


![image](https://github.com/user-attachments/assets/5606ef4a-34bf-4fcd-80a8-2633ed7ca30e)

![image](https://github.com/user-attachments/assets/4ac59aa5-eda3-4860-8692-bbdc6bffe354)
q
q
savez



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

### Assign an access Interface to VLAN ⚙️   

Assign interface GigabitEthernet 0/0/2 to Vlan 10

[switch1]`interface GigabitEthernet 0/0/2`      
[switch1-GigabitEthernet0/0/2]`port link-type access`       
[switch1-GigabitEthernet0/0/2]`port default vlan 10`       
[switch1-GigabitEthernet0/0/2]quit


### Configuring a trunk interface ⚙️ 

Assign interface GigabitEthernet 0/0/4 as a trunk interface and assign to vlan 10 and 20   

[switch1]`interface GigabitEthernet 0/0/4`   
[switch1-GigabitEthernet0/0/4]`port link-type trunk`    
[switch1-GigabitEthernet0/0/4]`port trunk allow-pass vlan 10 , 20`   •	Allow specific VLANS to this interface   
[switch1-GigabitEthernet0/0/4]`port trunk pvid vlan 10`    •	Set default VLAN for trunk interface.
[switch1-GigabitEthernet0/0/4]quit



![image](https://github.com/user-attachments/assets/140a57e1-cb21-46f5-a6d6-a73f7cd5f69c)


# Find out the connected devices to a switch 

## view the LLDP neighbors of the switch. 

<HUAWEI> system-view     
[HUAWEI] lldp enable     
display lldp neighbor        
display lldp neighbor brief           
display lldp neighbor interface XGigabitEthernet 2/2/4          

<HUAWEI> system-view      
[HUAWEI] interface gigabitethernet 0/0/1     
[Quidway-GigabitEthernet1/0/1] lldp enable       
Info: The LLDP is enabled on the port successfully.       

and     
 "display mac-address"           
 "display arp"             
 "display interface brief"            
 

# Find out a mac address

## searching for MAC address "0011-2233-4455":    
display mac-address 0011-2233-4455     

## Search for MAC addresses on interface GigabitEthernet 0/1/1,    
display mac-address GigabitEthernet 0/1/1     

## You can also search for MAC addresses associated with a specific VLAN.    
display mac-address vlan 10    
display mac-address vlan 4 GigabitEthernet 0/1/1    
display mac-address static vlan 2


![image](https://github.com/user-attachments/assets/810b73d1-386e-469f-a25b-1459ea29205c)

![image](https://github.com/user-attachments/assets/8651914c-6bd5-459e-9cce-11ceac1b9782)

![image](https://github.com/user-attachments/assets/780c58d4-3f06-4954-9e48-d935eb77bafe)


![image](https://github.com/user-attachments/assets/966f4f86-0529-401b-8553-b9d0ef8ac389)


![image](https://github.com/user-attachments/assets/09f8e033-a00d-4856-9249-d23a3dfbf4e2)

![image](https://github.com/user-attachments/assets/4c0ff4ab-3d75-460e-8239-809ecd8a4259)


