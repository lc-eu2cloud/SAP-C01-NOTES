## JSON101 - JavaScript Object Notation ##

#### JSON Introduction ####
JSON:  
* a lightweight data-interchange format: easy for humans to read & write; easy for machines to parse & generate 
* a JSON Object: an unordered set/list of key:value pairs enclosed in {&} (the equivalent of a dictionary in YAML)
* a JSON array: an ordered collection of values, comma separated & enclosed in [&] (the equivalent of a list in YAML)
* JSON supports representing values as string, object, number, array, true, false, null
* within AWS, JSON can be used within CloudFormation & for identity & resource policy documents
* #### Objects & Lists ####
  * every JSON document starts with a top-level JSON object (an unordered list of key:value pairs surrounded by {})
  * in this example, a top-level JSON object with 3 key:value pairs where each key ("cats","colors","numofeyes") has a corresponding value where the value is an array
![JSON array example](https://user-images.githubusercontent.com/88348559/197581414-60bd83bf-f469-454f-9012-253f40ec4353.png)
* #### Structure ####
  * a top-level JSON Object with 4 key:value pairs where each key ("roffle","truffles","penny","winkie") has a corresponding value where the value is a JSON object (these 4 key:value pairs are then 4 nested JSON objects)
![JSON Nested Object example](https://user-images.githubusercontent.com/88348559/197581649-0a6b203f-96d5-4767-989b-61d9c908b4b9.png)
  * summary: JSON objects can be nested within JSON objects, arrays can be ordered lists of JSON objects, & arrays can contain JSON objects within themselves
    * lets you create complex structures which can be used by applications to parse or store data & configuration
* #### CloudFormation ####
  * JSON Template Excerpt
![CloudFormation JSON template Example](https://user-images.githubusercontent.com/88348559/197581796-db429942-e8f2-4223-b8f9-67f112037c09.png)
  * additionally:
    * Type has a string value which defines the type of resource created by CloudFormation
    * BucketName is a key with a string value which sets the name of the s3 bucket which will be created
  * NOTE: indentation doesn't matter as everything in JSON is enclosed ({},[],or "")
