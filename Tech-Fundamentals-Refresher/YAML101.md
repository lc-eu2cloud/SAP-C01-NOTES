## YAML101 - YAML AINT MARKUP LANGUAGE ##

#### YAML Introduction ####
* YAML: human readable language that specifies a consistent format for data storage/transmission (data serialization) using Unicode character set
  * format: key:value pairs, lists, dictionaries
* #### key:value ####
  * YAML document: unordered collection of key:value pairs where each key has a corresponding value
    * YAML supports representing keys & values as strings, numbers, floating point, boolean, and null 
* #### lists ####
  * generally known as an ordered set of values (can be also be called arrays, programming language-dependent)
  * YAML can represent a list using a key where the value is a set of comma separated elements [&] <-inline format
  * can also be represented as "key:\n hyphen then the value"
    * values can be enclosed in "",'', or not (optional, all are valid), however enclosing allows you to be more precise & avoid confusion
    * indentation REALLY matters (ALWAYS uses spaces), for example, list items (denoted by hyphen) with same level of indentation are all part of the same list
      * YAML can represent nested lists using different levels of indentation 
 
* #### Structure (Dictionary) ####
* #### CloudFormation ####
