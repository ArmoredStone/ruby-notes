net/http
```
require 'net/http' # loads library

uri = URI('https://ruby-doc.org') # creates URI entity

http_request = Net::HTTP.new(uri.host, uri.port)
#where Net is a module defining the Net namespace and HTTP is a subclass

http_request.use_ssl = true # extending the parameters

response = http_request.get('/') #executing the request on '/' of host and storing it into response

puts response.body.force_encoding("ISO-8859-1")
# response output
```