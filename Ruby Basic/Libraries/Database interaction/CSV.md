Comma separated value

Ruby has CSV library to operate such files
```
CSV.open('path.txt').each do |inquiry|
	p inquiry
end
=> ["a","b","c"]
```
