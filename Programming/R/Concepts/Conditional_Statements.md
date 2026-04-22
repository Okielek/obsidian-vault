---
tags:
  - if
  - R
  - while
  - for
  - break
  - next
---
## `if`
checks if condition is satisfied if not doesn't execute the file. You can also add else after if to execute expr2 if and ony if condition is not satisfied. ^if
### Usage Example:
```r
if(condition1){
	expr1
} else if(condition2){
	expr2
} else{
	expr3
}
```
## `while`
Will expression as long as condtion1 is satisfied.^while
### Usage example:
```r
while(condition1){
	expr
}
```
### More info/Compatible functions
[[Conditional_Statements#break|break]] , [[Conditional_Statements#next|next]] 
## `for`
will iterate over any datatype that is iterable. ^for
### Usage example
```r
for(var in seq) {
	expr
}
```
### More info/Compatible functions
[[Conditional_Statements#break|break]] , [[Conditional_Statements#next|next]]
## `break`
Breaks any loop if called. ^break
### Usage example
```r
while(condition1){
	if(condtion2){
		break
	}
	expr
}
```
## `next`
Skips the current iteration. ^next
### Usage example
```r
for(x in y){
	if(condition){
		next
	}
	expr
}
```