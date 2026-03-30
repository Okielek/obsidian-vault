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



