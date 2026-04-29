---
tags:
  - R
  - data-structures
  - programming
  - list
  - vector
  - matrix
  - dataframe
---

## `c()`
Initialize a vector in R. 
#### additional info:
1. If you add v1 to v2 it will add like in numpy i mean it will do `new_v[i] = v1[i] + v2[i]` for each i. The same goes for any logical operation like: "-, *, ^, >, =". ^vector
```r
v1 -> [1, 2, 3, 4]; v2 -> [T, F, T, F] 
v3 -> v1[v2]                            # v3 = [1, 3]
```
1. `sum(vector)` returns the sum of the whole vector. 
## `list()`
A vector that let's you hold different datatypes in one place.^list
**Usage example:**
```r
my_list <- list(name_1 = int, name_2 = char, 
				name_3 = df)
my_list$name_3 # selects only df
```
## `matrix()`
Used to construct a 2D array containing only one data type. ^matrix
**Usage example:**
1.  Initializing a matrix:
```r
matrix(1:9, byrow = TRUE, nrow = 3) #this gives:
								#	1 2 3
								#	4 5 6
								#	7 8 9
```
2. Getting specific rows/columns
```r
matrix # (from prev example)
matrix[1:2, 1:2] # this will result in a matrix: 
											#  1 2
											#  4 5
```
## `data.frame()`
Let's you costruct your own DataFrame, every column will be the same lenght. ^data-frame
**Usage Example:**
```r
v1 <- c(1, 2, 3)
v2 <- c("a", "b", "c")
data.frame(v1, v2)
```
## `factor()`
You use this command to initialize factor factor is basically is our way of saying to or this variable will have a limited number of options f.e Sex: Male or Female. ^factor
**Usage Example:**
```r
temperature_vector <- c("High", "Low", "High","Low", "Medium")
factor_temperature_vector <- factor(temperature_vector, order = TRUE, levels = c("Low", "Medium", "High"))
factor_temperature_vector # Low < Medium < High
```
by using order = TRUE and then providing levels = vector we basically initialize a way of camparing the variables with each other.

### `seq()`
Returns a specified sequence of numbers. it takes 3 arguments `(begining, end, by)`
first 2 must be specified if `by` is 1 by default.
#### Usage example
```R
seq(0, 10, by = 2) #0 2 4 6 8 10
```
## `rep()`
Repeats one action x number of times.
### Usage example
```R
rep(c(1, 2, 3), times = 2) # 1 2 3 1 2 3 reapeats the whole vector
rep(c(2, 4, 6), each = 2) # 2 2 4 4 6 6 each element gets repeated twice
```

