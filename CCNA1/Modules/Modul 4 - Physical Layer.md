- The OSI physical layer provides the means to transport the bits that make up a data link layer frame across the network media.
- This layer accepts a complete frame from the data link layer and encodes it as a series of signals that are transmitted to the local media.

## ___PL. Standards___
- __The physical layer hardware, media, encoding, and signaling standards:__
	- International Organization for Standardization (ISO)
	- Telecommunications Industry Association/Electronic Industries Association (TIA/EIA)
	- International Telecommunication Union (ITU)
	- American National Standards Institute (ANSI)
	- Institute of Electrical and Electronics Engineers (IEEE)
	- National telecommunications regulatory authorities including the Federal Communication Commission (FCC) in the USA and the European Telecommunications Standards Institute (ETSI)

## ___Functional areas___
- __Physical Components__
	-  Electronic hardware devices, media, and other connectors that transmit the signals that represent the bits.
- __Encoding__
	- Method of converting a stream of data bits into a predefined "code”.
	- Method or pattern used to represent digital information.
- __Signaling__
	- Generating the electrical, optical, or wireless signals that represent the "1" and "0" on the media.

## ___Bandwidth___
- The capacity at which a medium can carry data.
-  Measures the amount of data that can flow from one place to another in a given amount of time.
- ##### ___Terminology___
	- __Latency__
		- Refers to the amount of time, including delays, for data to travel from one given point to another
	- __Throughput__
		-   The measure of the transfer of bits across the media over a given period of time.
		- __Factors__
			-  The amount of traffic
			- The type of traffic
			- The latency created by the number of network devices encountered between source and destination
	- __Goodput__
		-  The measure of **usable** data transferred over a given period of time.

## ___Copper Cabling___ 
- **Electromagnetic interference (EMI) or radio frequency interference (RFI)**
	- Signals can distort and corrupt the data signals being carried by copper media. Potential sources include radio waves and electromagnetic devices
	- __Counter:__  Copper cables are _wrapped in metallic shielding_ and *require proper grounding connections.*
- __Crosstalk__ 
	- Disturbance caused by the electric or magnetic fields of a signal on one wire to the signal in an adjacent wire. 
	- __Counter:__  Copper cables have _opposing circuit wire pairs twisted together_.
- ___Recommendations:___
	- Selecting the cable type or category most suited to a given networking environment
	- Designing a cable infrastructure to avoid known and potential sources of interference in the building structure
	- Using cabling techniques that include the proper handling and termination of the cables
#### ___Types___
- __Unshielded twisted-pair (UTP)__
	-  The twisting of wires helps protect against signal interference from other wires.
- __Shielded twisted-pair (STP)__
	- Provides better noise protection then UTP.
	- All pares wrapped in a foil shield and all are wrapped in an overall metallic braid of foil.
- __Coaxial cable__
	- Two conductors that share the same axis.
	- __Consists__
		- Copper conductor
		- Plastic insulation
		- Braided copper shielding _(Used as second wire and a shield)_
		- Outer jacket
	- __Used in__
		- __Wireless Installations__
			- Coaxial cables attach antennas to wireless devices.
		- __Cable internet installations__
## ___UTP Cabling___
- __Ways to limit the crosstalk__
	- __Cancellation__ - Pair wires in a circuit.
	- __Varying the number of twists per wire pair__ -
- ___Standards___ 
	- __TIA/EIA__
		- Cable types
		- Cable length
		- Connectors
		- Cable termination
		- Methods of testing cable
	-  __IEEE__
- ___Straight-through___
	- Used to interconnect two different devices _(PC to router, router to switch)_
	- __Standards__ - Both ends __T568A or T658B__
- ___Crossover___
	- Used to interconnect two similar devices
	- __Standards__ - One end __T568A and other T568B__
## ___Fiber-Optic Cabling___
- Commonly used to interconnect network devices.
- ___Usage___
	- Enterprise Network
	- Fiber-to-the-home (FTTH)
	- Long-Haul Network
	- Submarine Cable Network
- Two fibers were required to support the **full duplex operation** 
- 
#### ___Types___
- __Single-mode fiber (SMF)__
	- Is used in long-distance situations.
- __Multimode fiber (MMF)__
	- Uses LED emitter.
	- Popular in LAN's.
## ___Wireless Media___
- __Limitations__
	- Coverage Area 
	- Interference
	- Security
	- Shared medium
#### ___Types___
- __Wi-Fi(IEEE 802.11)__
- __Bluetooth (IEEE 802.15)__
- **WiMAX (IEEE 802:16)** - Uses a _point-to-multipoint topology_
- **Zigbee (IEEE 802.15.4)** - Used for industrial and Internet of Things (IoT) environments 
 