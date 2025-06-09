# ___Application Layer___
- Provides interface between __the applications__ and __the underlying network__.
- __Protocols__ - used to exchange data programs running on __source and destination hosts__.
	- __DNS__ - Domain Name System
		- Port: 53
	- __DHCP__ - Dynamic Host Configuration Protocol
		- Port: client 68, server 67
	- __BOOTP__ - Bootstrap Protocol
		- Port: client 68, server 67
	- __SMTP__ - Simple Mail Transfere Protocol
		- Port: 25
	- __POP3__ - Post Office Protocol
		- Port: 110
	- __IMAP__ - Internet Message Access Protocol
		- Port: 143
	- __FTP__ - File Transfere Protocol
		- Port: 20 to 21 
	- __TFTP__ - Trivial File Transfere Protocol
		- Port: client 69

## ___Peer-to-peer(P2P)___
Data accessed from _peer_ device.
- __P2P networks__ 
	- Two or more PC are connected together and share resources.
- __P2P application__
	- Allows a devices work as both a client and a server within the same commun.
	- __BitTorrent, Direct Connect, eDonkey, etc__
	- Some are based on __Gnutella__ - user share whole files

## ___Web and email___
- ___HTTP(s)___
	- Request/response protocols
	- __Message types:___
		- __GET__ - client request for data
		- __POST__ - uploads data files to the web server
		- __PUT__ - uploads resources (content) to the web server
	- ___Email Protocols___
		- __SMTP__ - require message __body and header__
		- __POP3__ - retrieve mail from mail server
		- __IMAP__ - keep messages on the server

## ___IP addressing system___
- ___Domain Name System(DNS)___
	- __Fully-qualified domain name(FQDN)__ - [http://www.cisco.com](http://www.cisco.com/)
	- Matches resource names and the numeric address.
	- __Message format:__
		- __A__ - An end device IPv4 address
		- __NS__ -An authoritative name server
		- __AAAA__(quad-A) - An end device IPv6 address
		- __MX__ - A email exchange record
	- __Message section:__
		- __Question__ - question for the name server
		- __Answer__ - Resource records answering the question 
		- __Authority__ - Resource records pointing toward an authority
		- __Additional__ - Resource records holding additional info.
	- __Hierarchy__
		- __Top-level domains:__ .com, .au, .org etc.
- ___Dynamic Host Configuration Protocol(DHCP)___
	- _For IPv4_ - Automates the assignment of all IPv4 networking parameters 
		(dynamic addressing)
	- __leas period__ - when it expire, server gets a __DHCPRELESE__ message the address is in reuse.
	- __Operations__
		- __DHCP discover(DHCPDISCOVER)__ - identify any available DHCP servers on the network.
		- __DHCP offer(DHPCOFFER)__ - replies on DHCP discover
		- __DHCP request(DHCPREQUEST)__ - message for explicit server and lease offer
		- __DHCP acknowledgement(DHCPACK)__ - server tell the client that lease has been finalized.
- ___File Transfer Protocol(FTP)___
	- Allow data transfers between a client and a server
	- __SMP(Server Message Block)__ - describes the structure of shared network resources.
		- _Functions_
			- Start, authenticate, terminate sessions
			- Control file and printer access
			- Allow a application to send or receive messages to or from other device
	- 