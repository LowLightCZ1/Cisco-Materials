- __Internet Control Message Protocol__

## ___Host Raechability___
- It's used to test the reachability of a host on the IP network.
- __Echo Request/Echo Reply__
## ___Destination and Service Unreachable___
- Used when a host or gateway receives a packet that it can't deliver.
- __Codes for IPv4__
	- 0 - Net unreachable
	- 1 - Host 
	- 2 - Protocol 
	- 3 - Port unreachable
- __Codes for IPv6__
	- 0 - No route to destination 
	- 1 - Communication with the destination is administratively prohibited
	- 2 - Beyond scope of the source address
	- 3 - Address unreachable
	- 4 - Port unreachable
## ___IPv6 Messages___
- __Router Solicitation(RS) Message__
	- Sent when booting up
- __Router Advertisement(RA) Message__
	- sent every __200 sec.__
	- Can include __Addressing information__ (prefix, DNS address, domain name)
- __Neighbor Solicitation (NS) Message__
	- Performing __duplicate address detection(DAD)__
- __Neighbor Advertisement (NA) Message__