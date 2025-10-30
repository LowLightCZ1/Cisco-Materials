# ___Switch Boot Sequence___
- Turn it on and allow it to go through __five-step boot sequence__
- __Steps__
	1. Switch loads _POST_(power-on self-test) stored in ROM
		- Tests __CPU, DRAM__ and the portion of the __flash device
	2. Loads __boot loader software__
	3. Perform __low-level CPU initialization__
		- Initialize the CPU _registers, the quality memory, speed_
	4. Initializes the __flash file system__
	5. Locates and load a default IOS OS software image into memory
- Use __BOOT environment variable__ to automatically boot 
- The startup-config file = __config.txt__, it's located in flash 
___Boot system global command___
``boot system flash:/path_to_the_file_system/IOS_file_name.bin``

## ___Switch LED Indicators___
1. __SYST__ - Shows if the system is receiving power and is functioning properly
2. __RPS(Redundant Power System)__ - Show if it's ready to provide backup power
3. __STAT(Port Status)__ 
4. __DUPLX__ - If green, the port is in full-duplex mod, if off, ports are in half-duplex mode
5. __SPEED__ - Indicates that the port speed mode is selected
	- OFF - 10Mb/s
	- GREEN - 100Mb/s
	- BLINKING GREEN - 1000Mb/s
6. __PoE(Power over Ethernet)__  

## ___System Crash Recover___
1. Connect a PC by console cable to the switch console port. Configure terminal emulation software to connect to the switch.
2. Unplug the switch power cord.
3. Reconnect the power cord to the switch and, _within 15 sec._, press and hold down the __Mode__ btn
4. Continue pressing the button until the System LED turns briefly ember
``set`` - View the path to the BOOT environment variable 
``flash_init`` - initialize the flash system

```
switch: set
BOOT=flash:/####/####.bin
(otput omitted)
switch: flash_init
Initializing Flash...
flash[0]: 2 files, 1 directories
flash[0]: 0 orphaned files, 0 orphaned directories
flash[0]: Total bites: ####
flash[0]: Bytes used: ####
flash[0]: Bytes available: ####
flash[0]: flashfs fsck took 10 second
...done Initializing Flash. 
```

``dir flash`` - View directories and files in flash

```
switch: dir flash:
Directory of flash:/

2 -rwx #### <date>                #######.bin
2 -rwx #### <date>                multiple-fs

```

``BOOT=flash`` - Command to change environment variable path in flash 

```
switch: BOOT=flash:######.bin
switch: set
BOOT=flash:######.bin
(otput omitted)
switch: boot
```
## ___Switch Management Access___
- Switch must have a __switch virtual interface(SVI)__ configured with an __IPv4 or IPv6__
- Able to access from remote network
- !!! Must be configured with a default gateway

## ___Switch SVI Configuration Example___
- __Step 1__ - Configure the Management Interface
```
S1# configure terminal
S1(config)# interface vlan 99
S1(config-if)# ip address 192.168.99.11 255.255.255.0
S1(config-if)# no shutdown
S1(config-if)# end
S1# copy runnig-config startup-config
```
>Note: Switch may be need to be configured for IPv6.
>Can use command `sdm prefer dual-ipv4-and-ipv6 defaault

- __Step 2__ - Configure the Default Gateway
```
S1# configure terminal [config t]
S1(config)# ip default-gateway 192.168.99.1
S1(config)# end
S1# copy running-config starup-config 
```

- __Step 3__ - Verify Configuration
```
S1# shoe ip interface brief
Interface     IP-Address     OK? Method   Status   Protocol
Vlan99        192.168.99.11  YES manual   down     down
(output omitted)
S1# show ipv6 interface brief
Vlan99                 [down/down]
     ########
     ########
(output omitted) 
```
# ___Configure Switch Ports___
- __Full-duplex__ - Receive AND Send
- __Half-duplex__ - Receive OR Send
> Gigabit Ethernet and 10 Gb NICs require __full-duplex__
- You can manually configure ports on switch with specific duplex and speed
_Port configuration_
```
S1(config)# interface FastEthernet0/1
S1(config-if) duplex full
S1(config-if) speed 100
S1(config-if) end
S1# copy running-config startup-config
```
## ___Auto-MDIX___
- __Automatic Medium-Dependent Interface Crossover__
- Automatically detect the required cable connection type

``mdix auto`` - Command for configuration MDIX

## ___Switch Verification Commands___
```
show interface 
show startup-config 
show running config 
show flash 
show version 
show history 
show ip(v6) interface 
show mac-address-table(mac address-table) 
```

## ___Verify Switch Port Configuration___
``show rinning-config`` - Verify that switch has been correctly configured
``show interface`` - Display status and statistics information on the network interfaces

# ___Secure Remote Access___

## ___Remote Operation___
- __Telnet__ 
	- Port: 23
	- Unsecure older protocol
- __SSH (Secure Shell)__
	- Port: 22
	- Secure better protocol

## ___Configure SSH___
```
S1# show ip ssh
- Verify that switch support SSH

S1(config)# ip domain-name ####
S1(config)# crypto key generate rsa
How many bits in the modulus [512]: 1024
S1(config)# username admin secret ccna
S1(config)# line vty 0 15 
S1(config-line)# transport input ssh 
S1(config-line)# login local 
S1(config-line)# exit
S1(config)# ip ssh version 2
```

# ___Basic Router Configuration___
```
Router# configure terminal
Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)# hostname R1
R1(config)# enable secret class
R1(config)# line console 0
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit
R1(config)# line vty 0 4
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit
R1(config)# service password-encryption
R1(config)#
```

## ___Dual Stack Topology___
- Type of interfaces supported by each.

## ___Router Interfaces___
 - Supports LANs and WANs
 - Interconnect different types of networks 
 - __G2 ISR__
	 - One or two integrated Gigabit Ethernet interfaces 
	 - __HWIC__ - Height-Speed WAN Interface Card slots
 - To be enable, an interface must be:
	 - Configured with at least one IP address 
	 - Activated - By default = shutdown, also must be connected to other device
	 - Description 

```
R1(config)# interface gigabiteternet 0/0/0
R1(config-if)# ip address #### ####
R1(config-if)# ipv6 address ####/##
R1(config-if)# description Link to LAN 1
R1(config-if)# no shutdown
R1(config-if)# exit 
R1(config)# interface gigabiteternet 0/0/1
R1(config-if)# ip address #### ####
R1(config-if)# ipv6 address ####/##
R1(config-if)# description Link to LAN 2
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# interface serial 0/0/0
R1(config-if)# ip address #### ####
R1(config-if)# ipv6 address ####/##
R1(config-if)# description Link to R2
R1(config-if)# no shutdown
R1(config-if)# exit
```

## ___Loopback interfaces___
- Logical interface that is internal to the router.
- Useful for testing and managing a Cisco IOS device
``Router(config)# interface loopback number``
``Router(config-if)# ip address ip-address subnet-mask``

# ___Verify Directly Connected Networks___
- __Commands__
	``show ip(v6) interface brief`` - Display a summary for all interfaces
	``show running-config interface "interface-id"`` - Displays the commands applied to the specified interface
	``show ip(v6) route`` - Display routing table
- Pipe __|__
	- __section__
	``show running config | section "line vty"``
	- __include__
	``show ip interface brief | inclide "up"`` - Includes all output lines that match the filtering expression
	- __exclude__
	``show ip inteface brief | exclude "unassigned"
	- __begin__
	``show ip route | begin "Gateway"``


