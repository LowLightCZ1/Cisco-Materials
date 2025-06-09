## ___Structure___
- 32- hierarchical addresses
- Made up a of __network portion__ and __host portion:__
	- __Network portion__ - Addresses must be identical for all devices in the same network
	- __Host portion__ - this bits must be unique for each host.

## ___Subnet mask___
- Identify the network/host portion of the IPv4 address
>Note:  __A default gateway__ - Required to reach remote network
>Note: __DNS__ - Required to translate domain names to IP addresses 

- __Network address__ - Represent a specific network. Device must have:
	- Same subnet mask
	- Same network bits as the network address
	- Located on the same broadcast domain 
- __Host address__ - Addresses that can be assigned to a device.
- __Broadcast address__ - address that it!s used to reach all devices in network. 

## ___Unicast___
- One-to-one communication with devices
- __Address range__: 1.0.0.1 - 223.255.255.255

## ___Broadcast__
- Communication with all devices in the network (one-to-all)
- __Broadcast packet__ - Destination IP with all ones (1) in the portion, or 32 one(1) bits.
>Note: Only IPv4 uses broadcast packet, IPv6 does not.

## ___Multicast___
- Range of multicast address: 224.0.0.0 - 239.255.255.255

## ___Public and Private Addresses___
 - __Public IPv4 Addresses__ - Are globally routed between __ISP__(Internet Service Provider)
- __Private IPv4 Addresses__ - Are used to assign addresses to internal hosts.

| Network Address and Prefix | RFC 1918 Private Address Range |
| -------------------------- | ------------------------------ |
| 10.0.0.0/8                 | 10.0.0.0 - 10.255.255.255      |
| 172.16.0.0/12              | 172.16.0.0 - 172.31.255.255    |
| 192.168.0.0/16             | 192.168.0.0 - 192.168.255.255  |
## ___Routing to the internet___
- When host sending packet that has source address __private__ and destination address __public(globally routable)__, packet bust __filtered(discarded)__ or __translated__ to a public address.
- __Network Address Translation (NAT)__ - Translate address from private to public
- __DMZ (Demilitarized zone)__ 

## ___Special Use IPv4 Addresses___
- ___Loopback addresses___
	- 127.0.0.0/8 (127.0.0.1 - 127.255.255.254)
	- Used by a host to direct traffic to itself
- ___Link-Local addresses___
	- 169.254.0.0/16 (169.254.0.1 - 169.254.255.254)
	- __Automatic Private IP Addressing(APIPA)__ - Used by Windows DHCP client to self-configure when there is no DHCP-server.
	- 