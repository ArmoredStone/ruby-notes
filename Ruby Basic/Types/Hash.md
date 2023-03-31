Hash is a colection of key-data pairs.

Methods: https://ruby-doc.org/3.1.2/Hash.html

Initialized using {}:
	`x = {key:data Object}`

Keys are symbolic elements (like method and class name references).

To retrieve data from hash:
`x[:key] => dataObject`

	x.keys 
	x.values 
returns array
 

	x.delete(:key)
deletes element by key 

```
x.delete_if 
do|key,value| condition end
``` 
deletes elements if condition is met 

* select
`hash.select(|key,data|condition)`
	returns a hash of elements of hash that match the condition