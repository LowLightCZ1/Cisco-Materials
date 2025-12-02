# ___Frame Forwarding___
- Based on the flow of the traffic
- __Ingress__ - Describe the port where the frame enters the device.
- __Egress__ - Describe the port that frame will use when leaving the device.

## ___Switch MAC Address Table___
- Switch must know which device exist on which port
- Table stored in __CAM(Content Addressable Memory )__ - Used in _high-speed_ applications
## ___Learn and Forward Method___
- __Two-step__ process
#### __Learn -Examining the Source MAC Address__
- Every frame is checked for now information to learn
- If the source MAC address doesn't exist in table, address and port are added to the table.
- if the source MAC address exist in table, updates the refresh time (default: 5 min.)
#### __Forward - Examining the Destination MAC Address__
- __Unknow unicast__ - forward the frame to all ports 

## ___Switching Forwarding Methods___
- __Store-and-forward switching__ 
	- Primary Cisco's LAN switching method
	- __Characteristic__
		- _Error checking_ 
		- _Automatic buffering_
- __Cut-trough switching__ 

# ___Collisions and Broadcast Domain___
- __Collision domain__ - Network segment that share the same bandwidth between devices
- 

