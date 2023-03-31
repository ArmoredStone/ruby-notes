`condition` structures: 
```
==  

<  

>  

>=  

<=  

!= 

a<=>b # 0 if a == b, 1 if a > b, -1 if a < b 

&& 

|| 
```
* if
```
if condition1
		action1
	elsif condition2
		action2
	else
		action3
	end
```
action1 if condition1 true
action2 if condition2 true
action3 if neither is true

* unless
	`unless condition`
true if condition is false

* ?
	`condition ? actioniftrue : actioniffalse`

* case
```
case workingVariable
when workingVariable condition1
	action1
when workinVariable conditio2
	action2
else
	action3
end
```
case block