## Decimal to Binary Conversion (IP Addressing) ##
### Human vs. Computer
**IPv4 Address Notation: Dotted Decimal & Binary**
* Human sees IPv4 address as dotted decimal: 4 decimal numbers, separated by periods, ranging from 0-255
* Computer sees IPv4 address as binary: 32 bit binary number (4 sets of 8 bits, separated by periods; 8 bits = byte/octet)
 
**Decimal IPv4 address => Binary IPv4 address**
* Conversion: work from left to right with each decimal number between the periods
* Example: 133.33.33.7 into binary notation (refer to Binary Position Table in diagram below)
  ![Binary Position Table](https://i.postimg.cc/NF1X7BD2/image18.png)
  1. Start at table position 1 & compare decimal number 133 to binary position value at position 1 (128)
  * if decimal number < binary position value (ie 128),  then current table position (ie 1) binary value is 0; move to next table position
  * if decimal number >= binary position value, subtract it from decimal number, binary value is 1; move to next table position
  2. 133 > 128, subtract 128 from 133, 5 is remaining decimal value, binary value is 1, move to table position 2 

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
