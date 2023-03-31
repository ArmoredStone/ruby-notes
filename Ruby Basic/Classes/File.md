Reading:

`File.open("filepath","r")`
	object for reading lines from file

`File.new("filepath","r")`
	open file for reading

While you don't need to close after opening file with `.open`, after creating an instance you better `instancename.close` after usage.

You can change delimiter it uses to read file.
	`File.open("filepath").each('delimiter'){ |line| codeblock }`
		by default it uses `newline` delimiter.

also possible:

`.open("filepath").each_byte`


`.open("filepath").each_char`

`.open("filepath").readlines`
	array of every line

not necessary to open, could be used class function `File.readlines`

Writing:

```
File.open("filepath","w") do |f|
	f.puts "Text"
end
```

Encodings

to open file with specific encoding:

`File.open("path.txt","r:utf-8")`

this encoding will be applied for all operations whether or not it was it's origin encoding

you can determine the base encoding by opening file for reading and running `.external_encoding` method

```
File.open("text.txt", "r:utf-8:iso-8859-1") do |f|
	f.external_encoding # => UTF8
	f.gets.external_encoding # => iso-8859-1
end
```
with such structure the data will be translated into iso-8859-1 from utf-8

`File.rename("old","new")`
`File.delete("path") == File.unlink("path")`

to construct filepath use
`File.join('a','b','c','d.txt') 
it joins directories based on system syntax

`File.expand_path("file_in_dir.txt") => full/path/to/file_in_dir.txt`

`File.mtime("path")`
	to get time of last modification of a file

`File.exist?("path") => true/false` 

`File.size("path")`
	=> byte size of the file if exists/error if doesn't exist
