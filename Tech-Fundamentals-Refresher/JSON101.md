## JSON101 - JavaScript Object Notation ##

#### JSON Introduction ####
* easy for humans to read & write; easy for machines to parse & generate (lightweight data-interchange format)
* JSON Object: unordered set of key:value pairs enclosed by {&} (YAML equivalent of dictionary)
* JSON array: ordered collection of values, comma separated & enclosed by [&] (YAML equivalent of list)
* JSON supports representing values as string, object, number, array, true, false, null
* within AWS, JSON can be used within CloudFormation & for identity policy documents

* #### Objects & Lists ####
  * each key ("cats","colors","numofeyes") has a value where the value is an array
![JSON Object array example](https://i.postimg.cc/bNpyTqG3/image.png)
* #### Structure ####
  * JSON Object with 4 key:value pairs with key ("roffle","truffles","penny","winkie") where corresponding value is JSON object (4 nested JSON objects)
![JSON Object example](https://i.postimg.cc/MKnnRWgN/image.png)
  * summary: JSON objects can be nested within JSON objects, arrays can be ordered lists of JSON objects, & arrays can contain JSON objects within themselves 
* #### CloudFormation ####

