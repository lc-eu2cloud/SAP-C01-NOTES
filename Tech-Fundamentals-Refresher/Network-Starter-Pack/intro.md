## Network Starter Pack - 0 - Intro ##

#### Networking Reference Points ####
* Local Networking - how data moves between devices on your local network (foundational to understanding how data moves across the internet from starting to ending point)
* Routing - how data moves across the internet from your network to somewhere else (AWS or Netflix) via many interconnected networks
* Segmenting, Ports & Sessions - components which ensure reliable data transfer used by your **applications** (another networking reference point)
* OSI 7-Layer Model - breaking up networking components into 7 layers (distinct components), starting at the bottom with physical networking & ending at the top with application networking
#### OSI 7-Layer Model ####
* since the OSI model is conceptual, not always how networking software is implemented, but provides a good foundation on how each component/layer works & interacts with the other layers
* 7 layers stacked on top of each other; you start with physical -> data link -> network -> transport -> session -> presentation -> then end at application 
* these 7 layers aka networking stack: software that does each of these functions in the OSI 7-Layer model
  * laptops, phones, wifi/cable routers, & servers, are some examples of devices that have networking stacks
* the OSI model is divided into 2 groupings:
  * media layers (physical, data link, network)
    * how data moves between point A & point B (ie on your local network or across the globe)
  * host layers (transport, session, presentation, application)
    * how data is segmented & reassembled for transport & formatted so that both sides of a network connection can understand it
* High-Level Conceptual OSI model overview
  * Layer 7: web browser at one end of the connection & web server at the other end of the connection
  * Layer 1: physical network cards/interfaces; any data from the web browser flows down through the layers at one end of the connection, arrives at the other end of the connection, then flows back up through the layers, to the web server software at the application layer
