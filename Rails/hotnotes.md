`rails new application_name`
	to generate a skeletal rails application

Main skeletal application folders:
	app/
Contains the controllers, models, views, helpers, mailers, channels, jobs, and assets for your application. You'll focus on this folder for the remainder of this guide.
	bin/
Contains the `rails` script that starts your app and can contain other scripts you use to set up, update, deploy, or run your application.
	config/
Contains configuration for your application's routes, database, and more. This is covered in more detail in [Configuring Rails Applications](https://guides.rubyonrails.org/configuring.html).
	config.ru
Rack configuration for Rack-based servers used to start the application. For more information about Rack, see the [Rack website](https://rack.github.io/).
	db/
Contains your current database schema, as well as the database migrations.
	Gemfile  
	Gemfile.lock
These files allow you to specify what gem dependencies are needed for your Rails application. These files are used by the Bundler gem. For more information about Bundler, see the [Bundler website](https://bundler.io).
	lib/
Extended modules for your application.
	log/
Application log files.
	public/
Contains static files and compiled assets. When your app is running, this directory will be exposed as-is.
	Rakefile
This file locates and loads tasks that can be run from the command line. The task definitions are defined throughout the components of Rails. Rather than changing `Rakefile`, you should add your own tasks by adding files to the `lib/tasks` directory of your application.
	README.md
This is a brief instruction manual for your application. You should edit this file to tell others what your application does, how to set it up, and so on.
	storage/
Active Storage files for Disk Service. This is covered in [Active Storage Overview](https://guides.rubyonrails.org/active_storage_overview.html).
	test/
Unit tests, fixtures, and other test apparatus. These are covered in [Testing Rails Applications](https://guides.rubyonrails.org/testing.html).
	tmp/
Temporary files (like cache and pid files).
	vendor/
A place for all third-party code. In a typical Rails application this includes vendored gems.

You should not `require` anything since Autoloading feature works on all files under `/app`
	You only need `require` for loading files under `/lib`

`bin/rails console` to enter irb-like environment with access to all our application schemas

CRUD
	Read
		since you don't need to import anything inside the `/app` folder
		You simply use Model.action to retrieve data from database.
	Create
		in controller 2 functions are created:
			`new`
				renders a view with form for creation a new inquiry for the database 
			  and
			`create`
				triggered on form submission, actully writes and validates the data for the database


`<!-- -->` is an html comment tag

