`Dir.chdir("path")` changes the directory
`Dir.pwd` => returns current directory
`Dir.entries("path")` => array of files and directories of path
`Dir.foreach("path")`=> same as entries but as iterator
`Dir. mkdir("name" or "fullpath")`=>creates a directory

*If you want to create an entire structure of directories, you must create them one by one from the top down.

`Dir.delete/unlink/rmdir("name" or "fullpath")`

*If a directory isn’t empty, you cannot delete it with a single call to Dir.delete. You need to iterate through each of the subdirectories and files and remove them all first

or use recursive deletion from fileutils

`FileUtils.rm_f("path")`

---

`require 'tmpdir'`

`Dir.tmpdir`=> path to temporary directory(which only exists for application runtime)

`File.join(Dir.tmpdir, "tmpfilename.txt")`
	to create a temporaryfile path for further creation of such


`require 'tempfile'`

`f = Tempfile.new('name')`
`f.path` => tmpdir/name
`f.close` => file deleted