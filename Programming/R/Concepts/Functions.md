---
tags:
  - R
  - functions
---
Function are a black box that take in arguments **(inputs)** and then accordingly to the function give out other arguments **(outputs)**. `input-> expression -> output` ^function
## `Defining Your own functions`
Last expression evaluated in an R function becomes return value.

### Usage example
```R
my_f <- function(x, y, z){
	x <- f(x)
	return(x)
}
```
## `Anonymous functions`
It's a concept of using a function without defining it. It's usefull for stuff like lapply() which needs a function to work.
### Usage example
```R
names <- lapply(split_low, function(x){x[1]})
```