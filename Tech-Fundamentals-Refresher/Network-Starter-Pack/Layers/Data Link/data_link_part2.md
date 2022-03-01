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
  * anything using layer 1 services just has visibility to layer 1 communication & there is no layer below it 😉
* Game communication between both laptops appears as layer 2 communication (physical communication at layer 1 is abstracted away)
![Layer 2: Game Example - CD (both laptops)](https://i.postimg.cc/HxQyJFG7/image15.png)

**CD (Collision Detection)**
* function: detect multiple devices transmitting at same time & reduce likelihood of it happening again on same layer 2 network
* how it works: starting from both laptops checking & not detecting a carrier signal
  1. Both laptops' layer 2 software instructs layer 1 to transmit (simultaenous transmission causing a collision)
  2. A jam signal is sent by all of the devices which detect it & a random backoff period occurs for each device
  3. Backoff period: time duration a device will not attempt to transmit; transmission retried after backoff period expires
  4. Random backoff goal: only one device will attempt to transmit, all network devices will see the carrier signal & wait to transmit
  * if collision still occurs, another backoff period occurs with a longer duration, reducing likelihood of another collision
* shows how layer 2 provides collision detection & collision avoidance (jam signal + random backoff period)

Summary: device to device communication
* Layer 2 frames generated by Layer 2 software at source side are passed to Layer 1 (raw data transmitted onto the physical medium)
* at destination side, raw data taken off physical medium, passed to Layer 2 software (interprets the frame)
* frame passed to Layer 3 (interprets the data inside frame's payload) 

**_Scenario:_** 2 devices running a game; left & right laptop connected using a network cable (shared physical medium)
* Layer 1 software running on a network card simply transmits any data it receives onto the physical medium (no media access control)
* Layer 2 provides controlled access to the physical medium (solves problem of both laptops sending data at the same time)
  * NOTE: electrical signals overlapping & interfering with each other result in a collision, corrupting both pieces of data
![Layer 2: Game Example - Collision](https://i.postimg.cc/cLCKkmNF/image10.png)
