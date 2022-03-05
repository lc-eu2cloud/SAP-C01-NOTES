## Network Starter Pack - 1 - Physical ##

#### Layer 1 - Physical ####
`Scenario: 2 laptops on a local network, want to play a local area network (LAN) game between both laptops`
* either connect both laptops to the same wifi network or use a physical network cable
* both laptops have network interface card & connected using a copper network cable:
  * point-to-point electrical shared medium between the two devices
  * piece of cable which can be used to transmit electrical signals between the two network interface cards
![Layer 1: Physical - Game Example](https://i.postimg.cc/vHDd51yn/image5.png)
* physical medium needs a way to carry unstructured (raw) information (solved by Layer 1 standards aka specifications)
* **specifications:**
  * define how to transmit & receive raw bit streams (1s & 0s) between a device & a shared physical medium
  * define voltage levels, timings, data rates, usable distances, modulation method, connector type on each end of physical medium
* in this scenario, both laptops have a shared understanding of the physical medium (copper network cable)
  * can use this physical medium to send & receive raw data
  * electrical signals are used (binary 1 defined as 1 volt & binary 0 defined as -1 volt)
  * if both network cards in both laptops use the same standard, then 0s & 1s can be transmitted onto the medium by the left laptop & received from the medium by the right laptop
* shows how 2 networking devices/2 network interface cards can communnicate at layer 1
* using OSI 7-layer model: layer X device understands & contains functionality for that layer & anything below it 
* layer 1 device just understands layer 1
#### Layer 1 - Physical - HUB ####
`Scenario: need to add 2 more devices/players for a total of 4 (can't connect to network cable with only 2 connectors)`
* 4 devices can connect to a 4-port hub (left & right laptop no longer connected directly like in previous scenario)  
![Layer 1: Physical - Game Example - 4-port hub](https://i.postimg.cc/W1t02Kfp/image7.png)
* since this hub has 4 ports, it has 2 ports free; it can accommodate the top & bottom laptops  
* hubs have 1 job: retransmit anything it receives on any of its ports to all of the other ports (including any errors & collisions)
* layer 1 is a broadcast medium: no individual device addresses (ie 1 laptop cannot address traffic directly at another)
* collision: corrupts any transmissions on the shared medium (only 1 device can transmit at a time & be readable to everything else)
* **Layer 1: additonal notes**
  * no media access control (no method of controlling which devices can trasmit) 
  * likelihood of collisions increases, the more layer 1 devices present on the same layer 1 network
  * not able to detect when collisions occur (network cards just transmitting via voltage changes on the shared medium)
    * not digital signal: instead an analog signal which can transmit binary data

`Layer 1 Takeaways from Scenario: how devices ACTUALLY communicate at a physical level`
* doesn't have any capability beyond the specifications it defines 
  * all devices will use specifications in order to transmit onto & receive from the shared medium
* network has 1 broadcast domain & 1 collision domain (ie hub retransmits everything, including collisions)
* networks tend not to scale very well (the more devices added to a layer 1 network, higher the chance of collisions & data corruption)
* fundamental to networking & needs layer 2 (runs over the top of a working layer 1 connection), in order to be useful  
#### Layer 1 - Physical - Lesson Summary ####  
`NOTE: Only layer 1 networking, not interacting with the other layers`
* focuses on the shared physical medium (the standards for transmitting onto & receiving from the shared medium)
* all devices in same layer 1 network need to use the same layer 1 medium & device standards
  * generally: a certain type of network card & cable, OR wifi cards using certain types of antennas & frequency ranges
* doesn't provide any form of access control on the shared medium
* doesn't provide any uniquely identifiable devices (no method for device-to-device communication)
    

