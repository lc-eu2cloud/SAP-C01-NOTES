## Network Starter Pack - 2 - Data Link - Part 1 ##

### Layer 2 - Data Link - Ethernet Frame
**Layer 2 Fundamentals**
* Layer 2 network requires a working layer 1 network to operate; can run on different types of layer 1 networks (cable,fiber,wifi) & provide the same layer 2 capabilities
* Frame: format for sending information over a layer 2 network
* MAC address: unique hardware address for every device on a network (generally: MAC address uniquely attached to a specific piece of hardware, not software assigned)
  * formed of two parts: 
    * **organizationally unique identifier** (OUI;assigned to network device manufacturers, each with separate OUI)
    * **network interface controller** (NIC)
  * intended to create a globally unique MAC address on a network card
 ![Layer 2: MAC Address](https://i.postimg.cc/hPJfQX20/image8.png)
* Ethernet frame can be transmitted onto shared physical medium by layer 1 (handles conversion to voltages,light,or RF -> sent across the medium, & received by other devices connected to that shared medium
  * layer 1 doesn't understand the frame itself (simply transmits raw data onto the physical medium)

**Parts of a Frame** 
* Preamble & Start Frame Delimiter (1)
* (2)
* (3)
* either connect both laptops to the same wifi network or use a physical network cable
* both laptops have network interface card & connected using a copper network cable:
  * a point-to-point electrical shared medium between the two devices
  * a piece of cable which can be used to transmit electrical signals between the two network interface cards
![Layer 1: Physical - Game Example](https://i.postimg.cc/vHDd51yn/image5.png)
* physical medium needs a way to carry unstructured (raw) information (solved by Layer 1 standards aka specifications)
* **specifications:**
  * define how to transmit & receive raw bit streams (1s & 0s) between a device & a shared physical medium
  * define voltage levels, timings, data rates, usable distances, modulation method, & connector type
* in this scenario, both laptops have a shared understanding of the physical medium (copper network cable) & can use this physical medium to send & receive raw data
  * electrical signals are used (binary 1 defined as 1 volt & binary 0 defined as -1 volt)
  * if both network cards in both laptops use the same standard, then 0s & 1s can be transmitted onto the medium by the left laptop & received from the medium by the right laptop
* this scenario shows how 2 networking devices/2 network interface cards can communnicate at layer 1
* using OSI 7-layer model: layer X device understands & contains functionality for that layer & anything below it (layer 1 device just understands layer 1) 
#### Layer 1 - Physical - HUB ####
Scenario (need to add 2 more devices or players for a total of 4, 4 devices can't connect to a network cable with only 2 connectors)
* 4 devices can connect to a 4-port hub (left & right laptop no longer connected directly like in previous scenario)
![Layer 1: Physical - Game Example - 4-port hub](https://i.postimg.cc/W1t02Kfp/image7.png)
* since this hub has 4 ports, it also has 2 ports free; it can accommodate the top & bottom laptops
* hubs have 1 job: anything it receives on any of its ports, is retransmitted to all of the other ports (including any errors & collisions)
* NOTE: layer 1 is a broadcast medium: no individual device addresses (ie 1 laptop cannot address traffic directly at another)
* a collision corrupts any transmissions on the shared medium (only 1 device can transmit at a time & be readable to everything else)
* Layer 1 has no media access control (no method of controlling which devices can trasmit)
  * the likelihood of collisions increases, the more layer 1 devices present, on the same layer 1 network
* Layer 1 is not able to detect when collisions occur (network cards are just transmitting via voltage changes on the shared medium) 
  * it's not digital: it's an analog signal which can transmit binary data 
* in theory, network cards can all transmit at the same time

Summary
* layer 1 doesn't have any capability beyond the specifications it defines (all devices will use specifications in order to transmit onto the shared medium, & receive from the shared medium)
* a layer 1 network has 1 broadcast domain & 1 collision domain (ie hub retransmits everything, including collisions)
* layer 1 networks tend not to scale very well (the more devices added to a layer 1 network, the higher the chance of collisions & data corruption)
* layer 1 is fundamental to networking (how devices ACTUALLY communicate at a physical level) & needs layer 2 (runs over the top of a working layer 1 connection), in order to be useful  
#### Layer 1 - Physical ####
Summary (only have layer 1 networking, not interacting with the other layers)
* Layer 1: focuses on the physical shared medium (the standards for transmitting onto the medium, & the standards for receiving from the shared medium)
* all devices in same layer 1 network need to use the same layer 1 medium & device standards (generally: a certain type of network card & cable, OR wifi cards using certain types of antennas & frequency ranges)
* doesn't provide any form of access control on the shared medium, & doesn't give us any uniquely identifiable devices (no method for device-to-device communication)
    
