## ___MAC Sublayer___
- __Data Encapsulation__
	- Ethernet Frame
	- Ethernet Addressing
	- Ethernet Error detection
- __Accessing the Media__
## ___Ethernet Frame Fields___
- Minimum size: 64 bytes
- Maximum size: 1518 bytes
- Size can be larger by adding a __VLAN tagging__.
- ___Detail__
	- __Preamble and SFD__ - Used for synchronisation between deceiving  and sending device.
	- __Destination MAC Address__
	- __Source MAC Address__
	- __Type/Length__
	- __Data__
	- __FCS__ 

## ___MAC Address__
- Used to identify the physical source and destination devices (NICs) on the local network segment.
-  is a 48-bit address
#### ___Types___
- __Unicast MAC__
- __Multicast MAC__
	- MAC address of 01-00-5E
	- It is flooded out all Ethernet switch ports except the incoming port.
	- It is not forwarded by a router.
- __Broadcast MAC__
	-  MAC address of FF-FF-FF-FF-FF-FF
	- It is flooded out all Ethernet switch ports except the incoming port.
	- It is not forwarded by a router.

## ___Forwarding Methods (Cisco Switches)___
- __Store-and-forward switching__
- __Cut-through switching__
	- __Fast-forward__ - Immediately forwards a packet after reading the destination address.
	- __Fragment-free___ - The switch stores the first 64 bytes of the frame before forwarding. Performing a small error check  to ensure that a collision has not occurred before forwarding the frame.
- 