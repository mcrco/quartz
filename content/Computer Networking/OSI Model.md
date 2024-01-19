Networking's purpose is for 2 hosts to share data with each other.

There are 7 layers:
1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

# Physical (L1)

- transports bits
- cables, WiFi, [[Network Entities and Devices#Devices|devices like repeaters and hubs]]

# Data Link (L2)

- puts and receives bits on physical layer, such as wires
- NIC (network interface cards), WiFi Access cards, [[Network Entities and Devices#Devices|switches]]
- "hop to hop" between physical devices
- addressing scheme is **Mac Address**
	- 48 bits as 12 hex digits
	- ex: 94:65:9C:4B:8A:E5
	- every NIC has unique MAC address
	- stored in packet header as intermediate step from one device to another through routers
		- part of [[Network Protocols#ARP|ARP]]

# Network (L3)

- "end to end"
- [[Network Entities and Devices#Devices|routers]]
- addressing scheme is **[[Network Entities and Devices#Entitites|IP addresses]]**
	- stored in packet header as source and destination IP address
		- part of [[Network Protocols#ARP|ARP]]

# Transport (L4)

- service to service
- many services in computer require internet traffic
	- L4 distinguishes these data streams
- addressing scheme: **ports**
	- 0-65535: **TCP** (reliability)
	- 0-65535: **UDP** (reliability)
	- also part of packet header for ownership between programs
	- servers listen for requests to pre-defined ports
	- clients have random port

# Session, Presentation, Application (L5-7)

doesn't seem too cool lol + apparently pretty vague??