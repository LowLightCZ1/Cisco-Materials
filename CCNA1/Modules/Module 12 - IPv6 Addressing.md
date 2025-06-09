- Successor to __IPv4__
- 340 __undecilion__ addresses
- developed by __IETF__
- __128 bits length__ 
- 

## ___IPv4/v6 Coexistence___
- ___Migration techniques___
	1. __Dual Stack__
		- Allows __IPv4/v6__ coexist in the same network segment.
		- Run both protocol stacks simultaneously
	2. __Tunneling__
		- Method of transporting __IPv6 packet__ over an __IPv4 network__ inside an packet.
	3. __Translation__
		- __Network Address Translation 64__(NAT64)
		- allows __IPv6__ devices to communicate with __IPv4__ devices using technique similar to NAT


## ___IPv6 Types__
- __Unicast__ - identifies an interface on en __IPv6-enabled__ device.
	- __Global Unicast Address__(GUA)
	- __Link-local Address__(LLA)
- __Multicast__ - used to send a single __IPv6__ packet to multiple destination.
- __Anycast__ - __IPv6__ unicast address that can be send to multiple devices
## ___Prefix length__
- Prefix == Subnet 
## ___IPv6 GUA___
- equivalent of public __IPv4__
- __Parts__
	- __Global routing prefix__(GRP)
		- Assigned by provider
		- __/48__ - common GRP
	- Subnet ID
		- identify subnets within its site.
	- Interface ID
		- equivalent of host portion in __IPv4__
- __Ways which a device can obtain an IPv6 GUA address(automatically)
	- Stateless Address Autoconfiguration(SLAAC)
	- Stateful DHCPv6
## ___IPv6 LLA___
- Enables to communicate with other __IPv6-enabled__ device on the same link
- __fe08::/10 range__
- Ways to obtain a LLA
	- __Statically__ - manually configured.
	- __Dynamically__ - device create its own __Interface ID__ or using the __Extended Unique Identifier (EUI)__ 

## ___IPv6 Dynamic Addressing___
- __Router Advertisement(RA)__
	- __IPv6__ router Ethernet interface
	- Router must be __enabled__ for __IPv6__ routing (not sett in default).
- ___ICMPv6 RA___ - suggestion to a device how to obtain __IPv6 GUA__.
	- __Network prefix/prefix length__
	- __Default gateway address__
	- __DNS address/domain name__
	- ###### ___Methods___
		1. __SLAAC__ - allows a device to create own GUA without DHCPv6
			- _stateless_ - no central servers
			- 
		2. __SLAAC + stateless DHCPv6 server__ 
		3. __Stateful DHCPv6__

## ___EUI-64 Process___
- __Extended Unique Identifier(EUI)__
	- Uses the __48-bit Ethernet MAC__ of a client, inserts another __16 bits__ in the middle of the MAC address to create a __64-bit Interface ID__.

## ___IPv6 Multicast___
- 