To get current state of iterator you need to "capture" it by assigning it a name using `|iteratorname|` after `do` keyword

* times
	```
	NUMBER.times do
	 action
	end
	```
	executes action NUMBER times

* upto/downto
	```
	N.upto/downto(otherN) do
		action
	end
	```
	increments/decrements N until it reaches otherN and does `action` for each increment/decrement

* step
	 ```
	 N.step(goal, step) do
		 action
	end
	```
	does `action` exact amount of times it takes `N` to reach `goal` with that `step`, starting from not changed `N`

* scan
```
	strinLiteral.scan(regularExpression) do |occurence|
		action
	end
```
does `action` on every occurence of `regularExpression` in `stringLiteral`, occurence also could be accessed with name of `occurence`

* while
	```
	while condition
		action
	end
	```
while `condition` is true the `action` will keep repeating

* until
	```
	until condition
		action
	end
	```
the loop ends when the `condition` is met true