Methods:
* `literal.sub(mask,replacement)`
	a method that replaces first occurence of `mask` with `replacement` in string `literal`
* `literal.gsub(mask,replacement)`
	a method that replaces all occurences of `mask` with `replacement` in string `literal`

## Finding the first match

_String.=~(Regexp)_ returns the starting position of the first match or nil if no match was found:

```
>> "abc 123 def" =~ /\d+/
=> 4

>> "abc def ghi" =~ /\d+/
=> nil

>> "found" if "123 456 789" =~ /\d+/
=> "found"
```

## Finding all matches

_String.scan_ returns matching strings as array of Strings:

get all matches for a regex without capture group
```
>> "123 456 789".scan(/\d+/)
=> ["123", "456", "789"]
```
assigning matches to variables
```
>> first, second, third = "123 456 789".scan(/\d+/)
```

regex with captures
```
>> "123 456 789".scan(/(\d\d)(\d)/)
=> [["12", "3"], ["45", "6"], ["78", "9"]]
```
_String.scan_ can also be used with a block:
ruby regex without captures
```
>> "123 456 789".scan(/\d+/) {|m| p m }
"123"
"456"
"789"
```
ruby regex with captures
```
>> "123 456 789".scan(/(\d\d)(\d)/) { |m| puts "#{m.inspect}, 1st capture: #{$1}" }
["12", "3"], 1st capture: 12
["45", "6"], 1st capture: 45
["78", "9"], 1st capture: 78
```

## Replacing matches

_String.gsub_ returns a new String with matches replaced, _String.gsub!_ changes the String directly:

Replacing with a string (use \1, \2 ... to refer to captures)
```
>> "123 456 789".gsub(/(\d+)/, '[\1]')
>> "123 456 789".gsub(/(\d+)/, "[\\1]")
=> "[123] [456] [789]"
```

_gsub_ can also be used with a block:

```
>> "123 456 789".gsub(/(\d+)/) { |m| "[#{m}]" }
>> "123 456 789".gsub(/(\d+)/) { |m| "[#{$1}]" }
>> "123 456 789".gsub(/(\d+)/) { |m| "[#{Regexp.last_match[1]}]" }
=> "[123] [456] [789]"
```

## Modifiers

```
/.*/m         multiline: . matches newline
/.*/i         ignore case
/.*/x         extended: ignore whitespace in pattern
```

Regular expressions by example
```
/a/           character 'a' 
/\//          character '/' (/\?*+{[.|()^$ need to be escaped with \)
/./           any character (including newline for /.../m)

/a?/          0..1 'a'
/a*/          0..n 'a'  
/a+/          1..n 'a'   
/a{2,7}/      2..7 'a'    
/a{2,}/       2..n 'a'    
/a{,7}/       0..7 'a'    

/a?bc?/       'b' or 'ab' or 'bc' or 'abc'
/a|bc/        'a' or 'bc'
/(a|b)c/      'ac' or 'bc'

/[abc]/       a or b or c
/[^abc]/      any character except a or b or c
/[a-cF-H]/    a or b or c or F or G or H

/\d/          any digit [0-9]
/\w/          any letters, numbers or underscores [a-zA-Z0-9_]
/\s/          any whitespace character (including newline for /.../m)

/\D/          any character except digits
/\W/          any character except letters, numbers or underscores
/\S/          any character except whitespace

/^abc/        abc after line start
/abc$/        abc before line end
```

https://www.ralfebert.com/snippets/ruby-rails/regex_cheat_sheet/
