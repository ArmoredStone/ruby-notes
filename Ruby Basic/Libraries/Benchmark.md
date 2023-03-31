```
require 'benchmark'

time = Benchmark.measure do
	codeblock
end

p time => time taken to do the codeblock

0.050000         0.040000             0.090000           ( 0.455168)
user CPU time, system CPU time, total CPU, and “real” time taken

Benchmark.bm do
	code block
	bm.report("flag1")
	codeblock
	bm.report("flag2")
	codeblock
end
```