https://ruby-doc.org/3.1.2/Array.html

Is a collection of any Objects.
You can access element by index starting with 0.
You can also access elements from the end with negative index.

You can push element into already defined array using `<<` or `push` method.

	pop
method to remove last element.

	join(separator)
to combine all elements into a string with defined `separator`

	empty?
returns true/false

you can add arrays.
or substract.

* each
```
	array.each do |el|
		action
	end
```
does an iteration for every element `array` has got in it, also current element could be accessed with `el`

* collect
```
	array.collect do |el|
		action on el
	end
```
does an iteration for every element `array` has got in it, and returns an array of modified `el`s

Array generators:
```
%w() array of strings 

%r() regular expression. 

%q() string 

%x() a shell command (returning the output string) 

%i() array of symbols (Ruby >= 2.0.0) 

%s() symbol 

%() (without letter) shortcut for %Q() 
```

* select
`array.select(|element|condition)`
	returns an array of elements of array that match the condition