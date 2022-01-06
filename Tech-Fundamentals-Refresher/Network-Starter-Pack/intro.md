## Network Starter Pack - 0 - Intro ##

#### Networking Reference Points ####
* Local Networking - how data moves between devices on your local network (foundational to understanding how data moves across the internet from starting to ending point)
* Routing - how data moves across the internet from your network to somewhere else (AWS or Netflix) via many interconnected networks
* Segmenting, Ports & Sessions - components which ensure reliable data transfer used by your **applications** (another networking reference point)
* OSI 7-Layer Model - breaking up networking components into 7 layers (distinct components), starting at bottom with physical networking & ending at the top with application networking
#### OSI 7-Layer Model ####
* since OSI model conceptual, not always how networking software is implemented, but provides a good foundation on how each component/layer works & interacts with the other layers
* 7 layers stacked on top of each other; start with physical -> data link -> network -> transport -> session -> presentation -> application 
* these 7 layers aka networking stack: software that does each of these functions in the OSI model
  * laptops, phones, wifi/cable routers, servers, etc., have networking stacks
* OSI model divided into groupings:
  * media layers (physical, data link, network)
    * how data moved between point A & point B (ie within local network or across the globe)
  * host layers (transport, session, presentation, application)
    * how data is segmented & reassembled for transport & formatted so that both sides of a network connection can understand it
* High-level OSI model overview
  * Layer 7: web browser at one end & web server at other end of connection 
