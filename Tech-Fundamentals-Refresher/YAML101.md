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
  * can also be represented as "key:\n space hyphen then the value"
    * values can be enclosed in "",'', or not (all are optional & valid), however enclosing allows you to be more precise & avoid confusion
    * indentation REALLY matters (ALWAYS uses spaces), for example, list items (ALWAYS denoted by hyphen) with same level of indentation (space hyphen) are all part of the same list
      * YAML can also represent nested lists using different levels of indentation 
 
* #### Structure (Dictionary) ####
  * dictionary: where a list item within a list has a structure of an unordered set of 1 or more key:value pairs
  * image below: key "adrianscats" is a list of dictionaries where each dictionary contains a 'name' key, with a value, 'color' key with a value, then for final list item, a 3rd element, a 'numofeyes' key:value pair
![list item:dictionary/structure example](https://i.postimg.cc/rF5BghY6/image.png)
  * values can be represented as strings, numbers, floating point, booleans, lists, dictionaries, or a combination of any of them
  * through YAML,
* #### CloudFormation ####
