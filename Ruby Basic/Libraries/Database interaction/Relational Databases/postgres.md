```
require pg

DB = Sequel.connect('postgres://user:password@localhost/dbname')

DB.create_table :people do
	primary_key :id
	String :first_name
	String :last_name
	Integer :age
end

people = DB[:people]

poepole.insert(:first_name="n",:last_name="M",:age=3)


person = Person.where(first_name: "Chris").first # returns a symlink to the database entry

```