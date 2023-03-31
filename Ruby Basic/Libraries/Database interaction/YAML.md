`require 'yaml'`

`Object`

`Object.to_yaml`
	returns a yaml string representing object

`yaml.load(yamlstring)`
	returns a containered object
		* Object classes used in yaml string should be in scope, unless they won't be working.

```yaml string example
---
- !ruby/object:Person
age: 45
name: Fred Bloggs
- !ruby/object:Person
name: Laura Smith
age: 23
```
