
Ruby Gems

ruby repository of libraries

gem list - lists installed gems

http://rubygems.org/ main gem repository

`gem install <name>` - gem installation
	you could add various options to specify version of gem you want or something else

after installing gem you could require for later usage

`gem update` to update all of your gems

`gem uninstall <name>` to uninstall

—

bundler is a tool for assembling dependencies of a project
it creates a gemfile which lists every gem required for project well being

gemfile example
```
source 'https://rubygems.org' # repository url
gem 'nokogiri' 
gem 'rack', '~>1.5' # specified version >1.5 but not 2.0
```

when you run
bundle install
in a directory with a gemfile file it will install/upgrade all gems to required versions

Gemfile.lock is a result of bundling, a list of gems and their versions

----

Creating a gem

create a folder with name of gem
inside
	a folder lib with all the code
	a folder test with all the tests
	a folder doc with all the documentation
	a folder bin with command line scripts if needed

in the main folder you create file.gemspec
with the specifications
https://guides.rubygems.org/specification-reference/https://semver.org/
```
Gem::Specification.new do |s|
	s.name = 'string_extend'
	s.version = '0.0.1'
	s.summary = "StringExtend adds useful features to the String class"
	s.platform = Gem::Platform::RUBY
	s.files = Dir.glob("//**")
	s.test_files = Dir.glob("test/*_test.rb")
	s.authors = ["Your Name"]
	s.email = "your-email-address@email.com"
	s.required_ruby_version = '>= 2.0.0'
end
```

after specification you build the gem

gem build specification_file.gemspec
from the gemspec file location

it will create a .gem file which is a 

then you can install it using

gem install name

RubyGems is a free public gem repository
it has to have a unique name
you can push it using 

gem push gemname