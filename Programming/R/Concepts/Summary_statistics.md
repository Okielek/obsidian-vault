---
tags:
  - summary
  - R
  - programming
  - rounding
---

## `mean()`
returns the average of a vector.
## `length()`
returns the length of a vector (if summable).
## `sum()`
Returns the sum of numbers specified.
### Usage example
```R
sum(c(1, 2, 3)) # 6
```
## `rowSums()`
Used to calculate the sum of each row in a matrix.
### Usage example
```r
my_matrix <- matrix(1:9, nrows = 3)
sum_matrix <- rowSums(my_matrix)
```
## `sd()`
Calculates [[01_Important_Definitions#^standard-deviation|standard deviation]]
## `abs()`
Changes a value to an absolute value as in always >=0.
## `round()`
Rounds the value to a specified number of digits. If not specified it will round to wholes.
### Usage example
```R
round(3.14, digits = 1) # 3.1
```





