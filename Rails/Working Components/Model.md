Model
	creation
		`bin/rails generate model Name name1:extension var2:text`
			Model names are singular
		creates a name.rb in /models
		creates a db migration file with schema for creating database with provided columns to the generator
			to migrate database:
				`bin/rails db:migrate`
	to save model object to database you need to initialize an object and call `.save` on it.


Model