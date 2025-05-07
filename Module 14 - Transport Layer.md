- Logical communication between application on different hosts.
- Link between _application layer_ and the lower layers responsible for network transmission
- __Two protocols:__
	- __TCP__ - Transmission Control Protocol
	- __UPD__ - User Datagram Protocol

#### ___Responsibilities___
1. __Tracking individual conversations__ 
2. __Segmenting data__ - Divide data into size blocks. Blocks == _Segment, Datagram_
3. __Add Header information__ 
4. __Identifying the Applications__ - Using _port number_ to identify
5. __Multiplexing__ 

### ___TCP,UPD Protocols__
- ___TCP___
	- Reliable, full-featured protocol
	- Ensures that all data arrives
	- __Connection-oriented protocol__
	- ___Reliability and Flow control___
		- Number and track data segments transmitted to a _specific host_ and _application_.
		- Acknowledge received data
		- Retransmit any unacknowledged data after a certain amount of time
		- Sequence data that might arrive in wrong order
		- Send data at an efficient rate that is acceptable by the receiver
	>__Note:__ TCP segmentating data
	- __Three-way hand shake__

___UPD___
- Connectionless, stateless protocol
- __Best-effort protocol__
>__Note:__ UPD divide data to datagram, same as segments
### ___Right protocol to right device___
- ___TCP___
	- Reliable, Resend lost data, Need acknowledgement
	- __SMTP/IMAP__(Email)
	- __HTTP/S__
	- __SSH__
- ___UPD___
	- Fast, Low overhead, Doesn't need a acknowledgement or resend lost data. 
	- __IP telephones(VoIP)__ 
	- __DNS__
	- __DHCP__
	- __TFTP__
## ___TCP protocol___
- ___Control Flags___
	- __FIN(finish)__
	- __ACK(acknowledgement)__
	- __URG(Urgent pointer field significant)__
	- __SYN(Synchronize sequence numbers)__
	- __PSH(Push function)__
	- __RST(Reset the connection when an error or timeout occurs)__
- ___Features___
	- __Establishes a Session__(Communication)
	- __Ensure reliable delivery__ 
	- __Provides Same-order Delivery__
	- __Support flow control__ 
- ___Header___
	- Segment = 20 bytes(160 bits)
	[Segment Header.png]
	[Výstřižek.png]
## ___UPD protocol___
- ___Features___
	-  Data is reconstructed in the order that it is received.
	- Any segments that are lost are not resent.
	- There is no session establishment.
	- The sending is not informed about resource availability.
- ___Header___
	- Datagram = 8 bytes(64 bites)
	![[Datagram header.png]]

## ___Port numbers___
- ___Socket Pairs___
	- __socket__ - Combination of _IP address and port address_
	- two sockets combine to form a _socket pair_: 192.168.1.5:1099, 192.168.1.7:80
- ___Groups__
	 ![Ports.png]
	- __Well-known ports:__
	![[well-known.png]]
