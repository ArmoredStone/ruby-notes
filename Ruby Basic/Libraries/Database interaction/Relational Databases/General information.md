`sequel` is a gem for connecting to remote databases

to work with remote dbs you still need a driver library for it:
	`pg`
	`mysql2`
	etc.

```
DB = Sequel.connect('postgres://user:password@localhost/dbname')
```
