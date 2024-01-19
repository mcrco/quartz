# Entitites

- **host**: any device that sends or receives traffic
	- **client**: requests
	- **server**: receives requests and returns data
		- any computer with server software
 - **IP address**: ID for hosts
	 - included in every packet as src and dst
	 - IPv4: 32 bits, 4 octets -> decimal number
	 - hiearchical
		 - example of country: first number can denote country branch, second number can denote division, third number can denote conference room, etc...
 - **network**: transports traffic between hosts
	 - logical grouping of hosts, like house, cafe, classroom, etc...
	 - can have **subnets**
	 - networks <-> networks via Internet

# Devices

- **repeater**: takes signal and amplifies it
- p2p connection doesn't work -> **hub**: multi-port repeater connecting many hosts
	- central node in graph, everyone connected to host
	- everyone receives all data
	- to separate groups of hosts, we need
- **bridge**: 2-port device connecting 2 hubs
	- know which hosts are in which side -> only lets packets to other hub when necessary
- **switches**: combination of hub and bridge
	 - learns which hosts on each port -> communication *within* network
	 - **switching**: moving data within networks
- **router**: communication *between* networks
	- traffic control point at center of networks -> good for filtering, security, etc...
	- learns which network are attached, aka **routes**
	- has IP address in every attached network, acts as gateway
		- example: laptop in one classroom's (A) switch is connected to router. To send traffic to another laptop in another classroom (B), packet goes from laptop -> switch -> router (gateway in A) -> router (gateway in B) -> switch -> laptop
	- **routing**: moving data between networks