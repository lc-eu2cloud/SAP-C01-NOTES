## Network Starter Pack - 1 - Physical ##

#### Layer 1 - Physical ####
Scenario
* 2 laptops on your local network & want to play a local area network (LAN) game between both laptops
* you need to either connect both laptops to the same wifi network or use a physical network cable (in this scenario: using a physical connection between both laptops)
  * both laptops have network interface card & are connected using a network cable
  * in this scenario, you're assuming the network cable used is a copper network cable 
    * a point-to-point electrical shared medium between the two devices
    * a piece of cable which can be used to transmit electrical signals between the two network interface cards
* a physical medium can be copper (uses electrical signals), fiber (uses light), or wifi (uses radio frequency or RF)
![Layer 1: Physical - Game Example](https://i.postimg.cc/vHDd51yn/image5.png)
* no matter what the type of physical medium used, it needs a way to be able to carry unstructured (raw) information
* what solves this? Layer 1 or physical layer standards known as specifications:
  * define how to transmit & receive raw bit streams (1s & 0s) between a device & a shared physical medium (in this scenario: a piece of copper network cable between 2 devices)
  * also define things like voltage levels, timings, data rates, usable distances, modulation method, & the type of connector on each end of the physical cable
  * in this scenario, mean both laptops have a shared understanding of the physical medium (cable)
    * both laptops can use this physical medium to send & receive raw data
    * for a copper cable, electrical signals are used
      * a certain voltage defined as binary 1 (1 volt) & a certain voltage defined as binary 0 (-1 volt)
    * if both network cards in both laptops use the same standard (meaning they both agree), then 0s & 1s can be transmitted onto the medium by the left laptop & received from the medium by the right laptop
    * how 2 networking devices/2 network interface cards can communnicate at layer 1
* additionally: using the OSI 7-Layer model, you would see that a layer X device understands & contains functionality for that layer & anything below it (unless it's a layer 1 device, which just understands layer 1) 
#### Layer 1 - Physical - HUB ####
Scenario
* in the previous scenario, 2 laptops used a point-to-point layer 1 link (or network cable) to communicate, but what if we need to add more devices? (2 more devices or players, for a total of 4)
* we can't connect these 4 devices to a network cable with only 2 connectors, but we can add a networking device called a hub (in this scenario, a 4-port hub)
![Layer 1: Physical - Game Example - 4-port hub](https://i.postimg.cc/W1t02Kfp/image7.png)
  * instead of the left & right laptop being connected to each other directly, are now connected to 2 ports on this hub
  * since this hub has 4 ports, it also means it has 2 ports free; it can accommodate the top & bottom laptops
* hubs have 1 job:
  * anything the hub receives, on any of its ports, is retransmitted to all of the other ports; including any errors & collisions (1)
    * conceptually, this hub creates a 4-connector network cable (one single piece of physical medium these 4 devices can be connected to)
* NOTE: for Layer 1 networking: there are no individual device addresses, 1 laptop cannot address traffic directly at another, as layer 1 is a broadcast medium
  * for example, any time the network card on the left laptop transmits onto the physical medium, everything else receives it
    * it's like shouting into a room with 3 other people, & not using any names (a limitation of layer 1, that's fixed by layer 2)
* it's possible that 2 devices might try to transmit all at once, if this happens, then there will be a collision
  * this corrupts any transmissions on the shared medium; only 1 device, can trasmit, at a time on a shared medium & be readable to everything else
* Layer 1 has no media access control, no method of controlling which devices can trasmit
  * 
