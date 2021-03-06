## Network Starter Pack - 3 - Network - Part 1 ##
### Layer 3 - Network
#### L2=>L3 - Building a Common L3 Network
**Scenario: 2 Layer 2 Local Area Networks (LANs) with geographic separation (LAN1 & LAN2 isolated from each other)**
![Layer 3 Networking Example: Beginning](https://i.postimg.cc/v82n0f0V/image22.png)
* each LAN only uses Layer 2, joined by direct point-to-point link, & use _same_ Layer 2 protocol to communicate locally
* PPP/MPLS/ATM: layer 2 protocols, suitable for long distance point-to-point links (Ethernet: Layer 2 protocol generally used locally)
* Layer 3 capabilities: can be added onto 1 or more Layer 2 networks (example Layer 3 protocol - Internet Protocol aka IP)
  1. allows for cross-network IP addressing & routing to move data between LANs without direct point-to-point links
  2. Routers (Layer 3 devices): move IP packets from source to destination via many intermediate networks across the internet
  * encapsulate IP packet inside an ethernet frame over a local network
  * hop by hop, remove frame encapsulation & add a new one around _same_ IP packet when it needs to be moved to a new network
* shows why Layer 3 protocols (ie IP) needed
![Layer 3 Networking Example: End](https://i.postimg.cc/HxhndGv9/image23.png)

#### Layer 3 - IP - Packet Structure
**IP Versions - v4** 
* source & destination IP address field (source: device IP, generates the packet; destination: packet's intended destination) 
* protocol field: generally contains data provided by Layer 4 protocol (ie ICMP, TCP, UDP)
  * Layer 4 protocol data inside a packet (ICMP:1,TCP:6,UDP:17)
  * means a destination's network stack's Layer 3 component will know which Layer 4 protocol to pass the intended data
* Time to Live (TTL) field: defines # of hops a packet can move through (max # of hops if packet can't reach destination)

**IP Versions - v6**
* source & destination IP address field: similar to version 4 but larger (more possible IPv6 addresses)
* protocol field: same as version 4 (data generally provided by Layer 4 protocol)
* hop limit field: similar to TTL field in version 4 IP packet (max # of hops a packet can cross before it's discarded)
![Layer 3 IP Packet Structure Example](https://i.postimg.cc/wxszDyx7/image24.png)
