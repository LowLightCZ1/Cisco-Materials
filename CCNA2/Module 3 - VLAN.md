# ___VLAN Definitions___
- VLAN provide segmentation and organizational flexibility.
- Devices in VLAN communicate as they were connected on the same cable.
- Based on __Logical__ connection more than on __Physical__
- Each VLAN is considered a separate logical network

## ___Benefits of VLAN___
- __Smaller broadcast domain__
- __Improved security__
	- Only users in the same VLAN can communicate together
- __Improved IT efficiency__
- __Reduced cost__
- __Better performance__

## ___Types of VLAN___
- ___Default VLAN___ (1)
	- All ports are assigned to VLAN1 by default
	- The native VLAN is VLAN1 by default
	- The management VLAN is VLAN1 by default
	- VLAN1 cannot be renamed or deleted
	``show vlan brief``
- ___Data VLAN___
	- VLAN's configured to separate user-generated traffic
- ___Native VLAN___ (99)
	- Traffic must be tagged with its VLAN ID
	- 802.1Q trunk port inserts a 4-byte tag in the Ethernet header frame
- ___Management VLAN___
	- Data VLAN configured specially for the __management traffic__ (SSH, Telnet, SNMP, HTTP(S))

# ___VLANs in Multi-Switched Environment___

## ___VLAN Trunks___
- Trunks allow all VLAN traffic to propagate between switches - enables devices on different switches communicated without router
- __Point-to-point__ link between two network devices that carries more than one VLAN

## ___VLAN Tags___
- __Tagging__ - Using IEEE 802.1Q standard
- 4-byte tag
- ___Tag Field___
	- Type - A 2-byte tag protocol ID (TPID) 0x8100
	- User priority - A 3-bit value that supports level or service implementation
	- Canonical Format Identifier(CFI) - A 1-bit, enables __Token Ring__ frames
	- VLAN ID (VID) - A 12-bit 

