## Network Starter Pack - 2 - Data Link - Part 2 ##
### Layer 2 - Data Link - CSMA/CD
#### Continuation from Part 1: 2 devices running a game; left & right laptop connected using a network cable (shared physical medium)
**Review**
* Layer 2 uses Layer 1 & needs it in place & working for Layer 2 network to be active
* now both laptops' networking stacks (networking software layers) have working Layer 1 & Layer 2 network
* Game communication: uses Layer 2 network (each device now has MAC address: hardware address for each network interface card)

**Transmitting Data: game on left laptop wants to send game data to game on right laptop**
* Starting point: left laptop's Layer 2 software creates Ethernet Frame (F1) & knows MAC address of right laptop
* right laptop's MAC address (ending in 5b:76, see diagram below) is in F1's destination MAC address field
* F1's payload contains the game data to send to game on right laptop

**CSMA (Carrier Sense, Multiple Access)**
* function: sense a carrier signal (seen on layer 1 network when any other network device is transmitting at that point in time)
* how it works: starting from left laptop's networking stack with Ethernet Frame (F1)
  1. Layer 2 is communicating with Layer 1; Layer 2 is looking for any signs of carrier signal on the Layer 1 network
  2. Layer 2 passes F1 to Layer 1 when it doesn't sense a carrier; Layer 1 simply sees F1 as a block of data to transmit
  3. Right laptop's layer 1 software receives raw bitstream transmitted onto the medium by left laptop & passes it to Layer 2
  4. Layer 2 software analyzes F1's destination MAC address field & sees right laptop's MAC address ("I'm the destination!")
  5. Layer 2 can now pass the data contained in F1's payload to the game
 ![Layer 2: Game Example - CSMA (left laptop)](https://i.postimg.cc/HsvwMktW/image12.png)
* shows how game communication can work using Layer 2: 
  1. using Layer 1 to transmit & receive raw data
  2. adding MAC addressing on top of Layer 1: allowing for device-to-device communication & adding media access control
* Example: Right laptop utilizing media access control (continuation of game scenario)
  1. Right laptop's layer 2 software creates Ethernet Frame (F2) to send game data to game on left laptop
  2. Right laptop attempts to transmit at same time left laptop is transmitting
  3. Right laptop's layer 2 software works with layer 1 to check for a carrier signal on the shared physical medium
  4. Carrier signal detected (left laptop is transmitting); right laptop's layer 2 software waits until carrier signal no longer detected
  5. Layer 2 passes F2 to Layer 1 once carrier signal is not detected, Layer 1 simply sees F2 as a block of data to transmit
  6. Left laptop's layer 1 software receives raw bitstream transmitted onto the medium by right laptop & passes it to layer 2
  7. Layer 2 software analyzes F2's destination MAC address field & sees left laptop's MAC address ("I'm the destination!")
  8. Layer 2 can now pass the game data contained in F2's payload to the game
![Layer 2: Game Example - CSMA (right laptop)](https://i.postimg.cc/T3h2Kqdf/image14.png)
* Without layer 2, layer 1 would simply transmit any data it receives onto the shared physical medium & cause a collision
* With layer 2, layer 1 is only instructed to transmit the frame once a carrier signal is not detected
* Before either laptop sends game data, the game data is encapsulated inside a frame's payload
* Before giving intended data back to the game on either laptop, it's de-encapsulated (frame's payload extracted from the frame)

**Abstraction** 
* OSI 7-Layer Model abstraction: anything _using_ layer X services has no visibility to anything below layer X (layers are independent)
  * anything using layer 1 services just has visibility to layer 1 communication (there is no layer below layer 1) 😉
* Game communication between both laptops appears as layer 2 communication (physical communication at layer 1 is abstracted away)
![Layer 2: Game Example - CD (both laptops)](https://i.postimg.cc/HxQyJFG7/image15.png)

**CD (Collision Detection)**
* function: detect multiple devices transmitting at same time on same layer 2 network & reduce likelihood of it happening again
* how it works: starting from both laptops checking & not detecting a carrier signal on the shared physical medium
  1. Both laptops' layer 2 software instructs layer 1 to transmit (simultaenous transmission causes a collision)
  2. A jam signal is sent by all devices which detect the collision & a random backoff period occurs on each device
  3. Backoff period: time duration a device will not attempt to transmit; transmission retried after backoff period expires
  4. Random backoff goal: only 1 device will attempt to transmit, all other network devices will sense a carrier signal & wait to transmit
  * if collision still occurs, another backoff period occurs with a longer duration, reducing likelihood of another collision
* shows how layer 2 provides collision detection & collision avoidance (jam signal + random backoff period)

#### Layer 2 using a Hub
**Hub Review**

Scenario: 4 devices connected to same 4-port hub (top,bottom,left,right)
* Hub: Layer 1 device, only sees physical data, doesnt't understand frames, instead a multiport repeater
* If top laptop sends frame **_destined_** for bottom laptop, hub only sees frame as raw data & repeats it to all the other ports
* left & right laptops receive the raw data, Layer 2 software analyzes the frame, sees it's not intended destination, & discards the frame 
* bottom laptop's layer 2 software sees it's the intended destination & passes on the game data to the game
![Layer 2: Game Example - Issues using a Hub](https://i.postimg.cc/cC1sPhcL/image16.png) 

Issues using a Hub  
* collisions will still occur even though a hub doesn't prevent a layer 2 network running on top of it & providing layer 2 capabilities
* hubs only understand layer 1, cannot take advantage of CSMA/CD & collision avoidance capabilities to avoid collisions
* solved by a networking device called a switch (layer 2 device: understands & contains functionality for layer 2 & layer 1)

#### Layer 2 using a Switch
Continuation of Game Scenario: same 4 devices now connected to same 4-port switch (each device has its own MAC address)
* Switch: Layer 2 device, has its own MAC address table & learns what's connected to each port over time
* `populate MAC address table (switch capability #1)`
* can interpret the frames it receives & sees the source & destination MAC addresses
* populates its MAC address table with each network device's MAC address & port it's connected to
  * results from switch seeing the source MAC address on the frame 
* generally: happens first time each laptop sends a frame & the switch receives it
* `Store & forward frames (switch capability #2)`
* With MAC address table populated, top laptop sends a frame (F1) intended for left laptop
* switch receives F1 at the port the top laptop is connected to (2 possibilities)
  1. forwards F1 to all of the other ports (doesn't know which port the destination MAC address is attached to)
  2. forwards F1 to a specific port (knows the port the destination MAC address ending in 5b:78 is attached to, eth3)
![Layer 2: Game Example - Using a Switch](https://i.postimg.cc/J0qwbDKD/image17.png)

`Layer 2 Using a Switch: Game Scenario Takeaways`
* Switches store & forward frames (receive, store, & forward based on MAC address table, then discard the frame)
* NOTE: Switches don't forward collisions, only valid frames (each switch port is a separate collision domain)
  * collisions (simultaneous transmission) can only occur between the device & the port it's connected to
* layer 2 is foundation for all networks (wifi, wired, & the internet) used daily
* internet: fundamentally a large collection of interconnected layer 2 networks

### Layer 2 - Data Link - Lesson Summary


