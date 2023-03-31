Is "an anonymous, nameless method or function"

You pass parameters into code block using:
	`|parameter|`
	or
	refer to `parameter` numerically using
	`_1 _2 _3`

To pass codeblock as parameter you need to add `&` before parameter name in the function that receiving code block.
```
def each_vowel(&code_block) 
	%w{a e i o u}.each do |vowel|
		code_block.call(vowel)  
	end
end
each_vowel { |vowel| p vowel}
```
	makes array of vowels and then executes codeblock on each of it 

same thing does yield but you pass code block without parameter thing

```
def each_vowel 
	%w{a e i o u}.each { |vowel| yield vowel }
end 
each_vowel { |vowel| puts vowel } 
```
output:
```
each_vowel {|vowel| p vowel}
"a"
"e"                                                          
"i"                                                          
"o"                                                          
"u"                                                          
=> ["a", "e", "i", "o", "u"]
```

You store code blocks in Proc objects:
```
a = Proc.new { code block actions}
a.call
```
