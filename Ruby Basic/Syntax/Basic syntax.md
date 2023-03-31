	print Object
prints a string contains of an object

Syntax consist of tabs and `end` words on the end of block.

* *`#` for comments
* `exit` to exit the program
Variable 
	> names must be a single unit (no spaces!); must start with either a letter or an underscore; 
	> must contain only letters, numbers, or underscores; and are case-sensitive

Constant is a variable that begin with a capital letter.

* `nil` is nothing

Variables have three types:
> Local
	exist inside a code block
```
	def method
		x = 2
	end
```
> Global
> 	exists everywhere in the application
```
	$variable
```
> Class
> 	accessible by classname
```
	@@variable
```
>Object
>	Accessible within an instance
```
	@variable
```


SHEBANGING

file.sh or file.rb:
	#!/usr/bin/ruby # ruby location
	p "works"
./file.sh => "works"

—

Getting information about environment:

RUBY_DESCRIPTION
ENV.to_hash # hash

—

=~ regular expression check => true/false

---

ARGV array contains passed parameters

---

Dynamic code execution EVAL

`eval "puts 2+2"`
	displayed 4, returned nil

you can assemble string expressions and evaluate them

---
To run shell commands from ruby use:

Kernel.system("ls") -> outputs result of ls in console window

x=`ls` or %x{ls} -> result of ls is saved into x, `` and %{} is same

---
To get Strings encoding
```
"str".encoding = >  #Encoding:asdasdas

change encoding using

"str".encode("encoding")

first lines of file
# shebang line 
# coding: utf-8
```
---

EXAMINE THREADS AND RSPEC

