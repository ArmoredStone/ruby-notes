Classes defined using:
	```class Name < ParentClass
		contents
	end```

* Constructor
```
	def initialize(param1,param2)
		@param1 = param1
		@param2 = param2
	end
```

* Class method
	method accessible by classname
```
	def self.test_method
		action
	end
```

* Instance method
	accessible in all of class instances
```
	def method
		action
	end
```


Inheritance applied by `< ParentClassName` on the definition of the class. Only singular inheritance is allowed.
Keyword `super` to access parent class.

You can override existing methods within class scopes.
```
class X
	class String
		def length
				20
			end
		end
	def test(string)
		string.length
	end
end
X.new.test => always 20
```

Keyword `private` to mark all that 
declared next to be kept private.
	or to pass symbols to this keyword to make methods private

Keyword `public` to stop action of `private` keyword.

Keyword `protected` reduces scope of accessibility to it's class.

Polymorphism:
```
We have a parent class `Animal` and three child classes `Dog`, `Cat`, and `Cow`. Each of these classes has a `speak` method, but they implement it differently. When we create an array of animal objects and call the `speak` method on each of them using `each`, the correct `speak` method for each object is called based on its class. This is an example of polymorphism in action - the same method name (`speak`) is used across multiple classes, but each class implements it differently.
```

Nested classes are accessed though an instance of outer class. Created when could not be used anywhere else.

Constants act like global variables but could be overriden in inner scopes 

To access inner scope constant InnerScope::ConstantName 

Keyword `require` to import code from another file.
if you want to require file from same directory use ./
	`require './filename'`
or use 
`require_relative 'filename'`
any of requires does not require .rb suffix
while
`load 'filename.rb'`requires it


Modules is a way of separating methods and giving different namespaces for same-called methods.
Methods from modules called by prefixing ex.: 
	`ModuleName.methodname`
Modules cannot have instances nor inherit from classes.

Modules are included to classes using keyword `include` to extend their fuctionality.


Struct is a way for creating data container "classes" with no parameter confirmation

```
Player = Struct.new(:name, :location)
player = Player.new(some, parameters)
```

From keyboard input:
`a = gets` 
	will get 1 line from standard input
`a = readlines`
	will receive lines until you press Ctrl+D
	