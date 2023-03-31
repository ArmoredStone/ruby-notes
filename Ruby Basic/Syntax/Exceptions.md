Exceptions are subclasses of Exception class.

—

use raise to raise exception in your own code

example: 

```
def initialize(name)
	raise ArgumentError, "No name present" if name.empty?
end
```

Any exception is a class and you could create your own exceptions

```
begin
	critical code
rescue => e
	p "saved #{e.class}"
end
```

rescue block executed if exception in begin block arise

```
catch(:exit_symbol) do
	some shit
	throw :exit_symbol if some_shit_happened
	end
end
```

they can be in different code block but have to operate same symbolic reference