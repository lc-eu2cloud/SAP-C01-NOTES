## Network Starter Pack - 2 - Data Link - Part 1 ##

### Layer 2 - Data Link - Ethernet Frame
**Layer 2 Fundamentals**
* Layer 2 network requires a working layer 1 network to operate; can run on different types of layer 1 networks (cable,fiber,wifi) & provide the same Layer 2 capabilities
* Frame: format for sending information over a layer 2 network
* MAC address: unique hardware address for every device on a network, formed of two parts:
  * **organizationally unique identifier** (OUI;assigned to network device manufacturers, each with separate OUI)
  * **network interface controller** (NIC)
  * together, intended to create a globally unique MAC address on a network card
 ![Layer 2: MAC Address](https://i.postimg.cc/hPJfQX20/image8.png)
* Ethernet frame can be transmitted onto shared physical medium by layer 1 
* layer 1 handles conversion to voltages,light,or RF -> sent across the medium, received by other devices connected to shared medium
* layer 1 doesn't understand the frame itself (simply transmits raw data onto the physical medium)

**Parts of a Frame** 
* (1) Preamble & Start Frame Delimiter: allows devices to know where the start of the frame is
* (2) Destination & Source MAC addresses: the MAC address in destination & source field of the frame
  * MAC address in destination MAC address field specifices network device a frame can be sent to & MAC address in source MAC address field is device address of the device transmitting the frame 
  * NOTE: inserting all F's into destination MAC address field sends a frame to all devices on local network (broadcast) & inserting a device's MAC address into source MAC address field allows it to receive replies 
* (3) EtherType: specfies which Layer 3 protocol is puttting its data inside a frame (might be IP or Internet Protocol, common example)
  * Layer 3 uses Layer 2 frames for device-to-device communication on a local network like Layer 2 uses Layer 1 to transmit raw bit streams across a shared physical medium
  * why a device receiving a frame at the other side of the communication, needs to know which Layer 3 protocol originally put its data into that frame
![Layer 1: Physical - Game Example](https://i.postimg.cc/vHDd51yn/image5.png)

Scenario: 2 devices running a game; left & right laptop connected using a network cable (shared physical medium)
* Layer 1 software running on a network card simply transmits any data it receives onto the shared medium (no media access control)
* Layer 2 provides controlled access to the physical medium (solves problem of both laptops sending data at the same time)
  * NOTE: electrical signals overlapping & interfering with each other results in a collision, corrupting both pieces of data
![Layer 2: Game Example - Collision](https://i.postimg.cc/cLCKkmNF/image10.png)
