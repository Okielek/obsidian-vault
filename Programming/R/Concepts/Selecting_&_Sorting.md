### `subset()`
Let's You create a subset of your database with specific conditions.
```r
subset(my_df, subset = some_condition)
subset(my_df, subset = column_name < 1)
```
### `order()`
Let's you sort according to a certain variable.
**Usage example:**
```r
a <- c(100, 10, 1000)
order(a)
[1] 2 1 3
a[order(a)]
[1] 10 100 1000
```
## `sort()`
Sorts the vector by default in ascending order.
### Usage example
```R
sort(c(2, 3, 1)) # 1 2 3
sort(c(2, 3, 1), decreasing = TRUE) # 3 2 1 
```
## `rev()`
### Usage example
Reverses the order of a vector.
```R
rev(c(3, 2, 1)) # 1 2 3
```
## `which()`
**Returns indices of TRUE values** in a logical vector.
### Usage example
```R
x <- c(10, 20, 30, 40)
which(x > 25) # [1] 3 4
```


