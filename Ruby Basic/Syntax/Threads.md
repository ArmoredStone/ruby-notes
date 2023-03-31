Threads

```
threads = [] # array for the threads
10.times do  # generate 10 threads
	thread = Thread.new do # with same codeblock
		10.times { |i| print i; $stdout.flush; sleep rand(2) }
  end
  threads << thread # add thread to array
end
threads.each { |thread| thread.join }
```


The join method makes the main program wait until a thread’s execution is complete before continuing. In this way, you make sure all the threads are complete before exiting


`Thread.list to list all threads running`

—

Fiber is a fully scheduled thread

```
sg = Fiber.new do
	s = 0
	loop do
		square = s * s
		s += 1
		s = Fiber.yield(square) || s
	end
end
```
puts sg.resume
puts sg.resume
puts sg.resume
puts sg.resume
puts sg.resume 40