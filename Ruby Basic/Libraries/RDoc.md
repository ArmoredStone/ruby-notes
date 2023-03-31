It generates structured html documentation after scanning through source code files.

You can leave comments before initializing stuff and RDoc will grab these comment into documentation

https://ruby.github.io/rdoc/

—

RDoc could format all the rb files in the directory to create project documentation

You can use tabs and * in your comments to create lists and format the output

—
```
add #:nodoc: all to not document the whole thing

or

#--
# the text in comments between these flags won't be included
#++ 
```
RDoc doesn’t process comments that are within methods
—

CLI Options

```
--all to process all methods, not only public
--fmt choose format
--help help
--main <name> choose name that will appear on top of index
```