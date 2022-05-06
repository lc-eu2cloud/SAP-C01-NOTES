## Network Starter Pack - 3 - Network - Part 2 ##
### Layer 3 - Network
#### IP Addressing(v4) - IPv4
**Parts of an IP address (Network & Host)**
* network: IP network an IP address belongs to (ie 133.33)
* host: represents hosts/devices on an IP network (ie 3.7, one device, a laptop)

**Differentiating between IP networks**
* two different IP addresses with same network part are on the same IP network (if not, they're on different IP networks)
* Example: 133.33.3.7 <- /16 prefix (first 16 bits represent network part, remaining 16 bits represent host part) 
* IP address (133.33.33.37) network part matches network part of 1st IP address (133.33) -> on same IP network
* local devices - same IP network (network part of IP addresses match)
* remote devices - different IP network (network part of IP addresses don't match)

**Assigning IP Addresses (Static or Dynamic)**
* Static: IP addresses assigned by humans 
* Dynamic: IP addresses assigned by network servers running DHCP server software (Dynamic Host Configuration Protocol)
* IP addresses need to be unique (globally & especially on a local network) or bad things happen

**Subnet Mask**
* configured on L3 interfaces along with IP addresses (ie 1.2.3.4 255.255.255.255)
* default gateway: IP address on local network; packets forwarded to this IP address when intended destination not a local IP address
* subnet masks allow IP devices/hosts to know if communication with another IP device is on same network or not
  1. local network - IP devices/hosts attempt to communicate directly
  2. remote network - IP devices/hosts need to use default gateway
* 

#### L3 - Route Tables & Routes
**Subsection**
* xx
* xx
* xx

**Subsection**
* xx
* xx
* xx

**Subsection**
* xx
* xx
* xx
#### Section
**Subsection**
* xx
* xx
* xx

**Subsection**
* xx
* xx
* xx

**Subsection**
* xx
* xx
* xx
#### Lesson Summary Section
**Subsection**
* xx
* xx
* xx
