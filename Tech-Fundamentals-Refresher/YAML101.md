## YAML101 - YAML AINT MARKUP LANGUAGE ##

#### YAML Introduction ####
* YAML: a human readable data serialization language that specifies a consistent data structure conversion format for data storage/transmission using a Unicode character set
  * format: key:value pairs, lists, dictionaries
* #### key:value ####
  * in a YAML document: you will find an unordered collection of key:value pairs where each key has a corresponding value
    * YAML supports representing keys & values as strings, numbers, floating point, boolean, and null 
* #### lists ####
  * generally known as an ordered set of values (can be also be called arrays, programming language-dependent)
  * YAML can represent a list using a key where the value is a set of comma separated elements [&] <- the inline format
  * can also be represented as "key:\n space hyphen then the value"
    * values can be enclosed in "",'', or not (all options are valid), however enclosing allows you to be more precise & avoid confusion
    * indentation REALLY matters (ALWAYS uses spaces), for example, list items (ALWAYS denoted by hyphen) with same level of indentation (space hyphen) are all part of the same list
      * YAML can also represent nested lists using different levels of indentation 
* #### Structure (Dictionary) ####
  * dictionary: a structure of an unordered set of 1 or more key:value pairs
  * image below: key "adrianscats" is a list of dictionaries where each dictionary contains a 'name' key, with a value, 'color' key with a value, then for final list item, a 3rd element, a 'numofeyes' key:value pair
![list item:dictionary/structure example](https://i.postimg.cc/rF5BghY6/image.png)
  * values can be represented as strings, numbers, floating point, booleans, lists, dictionaries, or a combination of any of them
* through YAML, key:value pairs, lists, & dictionaries allow you to build complex data structures in a human readable way (e.g. database of someone's cats)
* YAML files can be read into or written out by an application, & commonly used for storage/transmission of configurations 
* #### CloudFormation (CFN) ####
  * YAML template (image below):
    * 'Resources' section which is a dictionary, within it a key 's3bucket', which is also a dictionary containing 'Type' & 'Properties' keys
      * Type has a string value, while Properties is a dictionary containing 'BucketName' where BucketName is a key with value of "ac1337catpics" (string)
  ![CFN yaml template excerpt](https://i.postimg.cc/7ZzQsg3M/image2-resize.png)
    * indentation levels (image above - highest level of indentation -> lowest):
      * 'BucketName' is nested within 'Properties'
      * 'Type' & 'Properties' with same level of indentation, are nested within 's3bucket'
      * 's3bucket' is nested within 'Resources'
      * 'Resources' is a top-level key:value pair within the YAML template
    * Summary:
      * 'Resources' is a key:value pair where the value is a dictionary with 1 key:value pair (s3bucket)
      * 's3bucket' is a key:value pair where the value is a dictionary with 2 key:value pairs (Type & Properties)
        * 'Type' is a key:value pair where the value is a string which controls what type of resource is created (in this example, a s3 bucket)
        * 'Properties' is a key:value pair where the value is a dictionary with 1 key:value pair (BucketName)
          * 'BucketName' is a key:value pair where the value is a string that controls the name of the s3 bucket (the physical resource that will be created by CloudFormation)  
