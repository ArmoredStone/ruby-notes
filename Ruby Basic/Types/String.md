Is a sequence of literal characters withing `""`.

Basic methods
https://ruby-doc.org/3.1.2/String.html

```
For multiline string literal use:
%qdelimitertext
some text
textdelimiter


Possible delimiters: <>, (), !!, although {} are recommended.

or

<<YOUR_DELIMITERNAME
to setup your own delimiter for multiline string literals
YOUR_DELIMITERNAME
```

```
Interpolation
x = y = "a"
n = "#{x} + #{y} = #{x+y}"
p n > "a + a = aa"
```

`"text" + "text" -> "texttext" `
	concatenation
`"text".length -> 4
	returns length of string 
`"text".upcase -> "TEXT" `
	returns uppercase of text 
`"text".capitalize -> "Text"`
	capitalize text 
`"TEXT".downcase -> "text"`
	downcase text 
`"text".chop(N) -> "tex"`
	remove last character 
`"text".next -> "texu"`
	sets last character to next by code 
`"text".reverse -> "txet"`
	reverse the string 
`"text".sum -> 453`
	sum of char codes?? 
`"TeXt".swapcase -> "tExT" `

`"text".split(regularexpression)`
	splits a literal into array by the occurences of regular expression

You can escape special characters by putting `\` before them. 

You can use `.inspect` method to get string representation of different Objects if they got this method implemented.

Tail call:
`"Test".upcase.reverse -> "TSET" `
`"Test".upcase.reverse.next -> "TSEU" `

Many methods have equivalents which end in `!` which actually modify the string itself.