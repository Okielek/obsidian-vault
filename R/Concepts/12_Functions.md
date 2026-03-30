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
