- Prepares network data for the physical layer.
- __What does it do:__
	- Enables upper layers to access the media.
	- Accepts data and encapsulates them into Layer 2 frame.
	- Controls how's data places and received on the media.
	- Performs error detection and rejects any corrupt frame.
#### ___Sublayers___
- __Logical Link Control (LLC)__
	- Communicates between _the networking software at the upper layer and the device hardware at the lower layer.
	-  It places information in the frame that identifies which network layer protocol is being used for the frame.
- __Media Access Control (MAC)__
	- Data encapsulation an media access control.
	- Data Link layer addressing.
	- __Data encapsulation__
		- __Frame delimiting__ - Synchronization between the transmitting and receiving nodes.
		- __Addressing__
		- __Error detection__
#### ___Standards___
- Institute of Electrical and Electronics Engineers (IEEE)
- International Telecommunication Union (ITU)
- International Organization for Standardization (ISO)
- American National Standards Institute (ANSI)
#### ___Topologies__
- __Physical Topologie__ 
- __Logical Topologies__
- __WAN Topologies__
	- Point-to-point
	- Hub and Spoke - WAN's version of star topologie.
	- Mesh
- __LAN Topologies__
	- Bus - All end systems are chained to each other and terminated in some form on each end.
	- Ring - End systems are connected to their respective neighbor forming a ring.
#### ___Half and Full Duplex___
- __Half-Duplex__ -  Allows only one device to send or receive at a time on the shared medium.
- __Full Duplex__ - Both devices can simultaneously transmit and receive on the shared media.
#### ___Access Control Methods___
- LAN's and WAN's  = Multiaccess networks
- Can have two or more end devices attempting to access the network simultaneously.
- **Contention-based access**
	- All nodes are operating in half-duplex.
	-  __CSMA/CD (Carrier sense multiple access with collision detection)__ are used on legacy bus-topology Ethernet LANs
	- __CSMA/CA (Carrier sense multiple access with collision avoidance )__ are used on Wireless LANs
- **Controlled access**
	- Legacy Token Ring
	- Legacy ARCNET
#### ___The Frame___
- __Fields__
	- __Frame start and stop indicator flags__ - Beginning and end limit.
	- __Addressing__ - Source and destination
	- __Type__ - Layer 3 protocols in field
	- __Control__  
	- __Data__
	- __Error detection__ 

1. Accepts a frame from a medium
2. De-encapsulates the frame
3. Re-encapsulates the packet into a new frame
4. Forwards the new frame appropriate to the medium of that segment of the physical network