## Decimal to Binary Conversion (IP Addressing) ##
### Human vs. Computer
**IPv4 Address Notation: Dotted Decimal & Binary**
* Human sees IPv4 address as dotted decimal: 4 decimal numbers, separated by periods, ranging from 0-255
* Computer sees IPv4 address as binary: 32 bit binary number (4 sets of 8 bits, separated by periods; 8 bits = byte/octet)
 
**Decimal IPv4 address => Binary IPv4 address**
* Conversion: work from left to right with each decimal number between the periods
* Example: 133.33.33.7 into binary notation (refer to Binary Position Table in diagram below)
  ![Binary Position Table](https://i.postimg.cc/NF1X7BD2/image18.png)
  1. Start at table position/column 1 & compare decimal number 133 to binary position value at position 1 (128)
  * if decimal number < binary position value (ie 128),  then current table position (ie 1) binary value is 0; move to next table position
  * if decimal number >= binary position value, subtract it from decimal number, binary value is 1; move to next table position
  2. 133 > 128, minus 128 from 133, 5 is new decimal value, column 1's binary value is 1, move to table position 2/column 2
  3. Repeat process (rule #1 in diagram above) for decimal value 5
  4. 5 < 64 (column 2's binary position value), column 2's binary value is 0, move to next column
  5. 5 < 32, 16, & 8, binary value is 0 for those corresponding table positions/columns
  6. 5 > 4 (column 6's binary position value), minus 4 from 5, 1 is new decimal value, column 6's binary value is 1, move to next column
  7. 1 < 2 (column 7's binary position value), column 7's binary value is 0, move to next column
  8. 1 = 1 (column 8's binary position value), minus 1 from 1, 0 is new decimal value, column 8's binary value is 1, process is finished
* shows how decimal value 133 (one part of IPv4 address) converted to binary number (10000101)

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
