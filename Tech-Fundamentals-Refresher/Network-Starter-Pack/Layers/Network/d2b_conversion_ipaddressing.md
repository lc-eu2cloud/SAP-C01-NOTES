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
* shows how decimal value 133 (one part of the IPv4 address) converted to binary number (10000101)
![End of Decimal to Binary Conversion Example](https://i.postimg.cc/hPvhG4By/image19.png)

**Binary IPv4 Address => Decimal IPv4 Address**
* Conversion: from left to right with each octet between the periods
* Example: 10000101 into decimal notation (refer to Binary Position Table in diagram below)
![Binary Position Table](https://i.postimg.cc/jSvjxjq2/image20.png)
  1. for each octet (8 bits), check for 1 or 0 in each binary bit position (start at position 1, end at position 8)
  * if 1, write corresponding binary position value (ie 128), add "+" then move to next binary bit position (ie position 2)
  * if 0, write 0 after "+" in the equation (128+0), add "+" after 0, then move to next binary bit position (ie position 3)
  2. repeat process until final bit position (position 8) is checked (add 1 or 0 to equation, ie 1)
  3. sum the values in equation together (128+0+0+0+0+4+0+1) to obtain the result (133)
* shows how 1st octet (10000101) converted to decimal value 133 (1st part of the IPv4 address)
* repeat process to convert remaining octets (shown above) to decimal values (33,33,7) & get dotted decimal IPv4 address (133.33.33.7)
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
