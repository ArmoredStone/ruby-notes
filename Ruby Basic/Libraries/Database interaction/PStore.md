a way to save the object instances to disk in hash for future reassembling

Putting
```
require 'pstore'
store = PStore.new("storagefile")
store.transaction do # start a transaction
	store[:people] ||= Array.new # assigns that :people symbols to an array
	store[:people] << fred
	store[:people] << laura
end
```

Retrieving
```
require 'pstore'
output = Array.new
store = PStore.new("storagefile")
store.transaction do
	output = store[:people]
end
```
