## Comparison operators
- `==` equal
- `!=` not equal
- `<` less than
- `<=` less or equal
- `>` greater than
- `>=` greater or equal
## Logical operators
- `&` AND
- `|` OR
- `!` NOT
### More info:
1. If any of these operators are used on a datatype that stores multiple entries then it preserves the structure wim: 
```r
x <- c(1, 2, 3)
x >1 # (FALSE, TRUE, TRUE)
```
## Special
- `&&` — AND (first element only)  
- `||` — OR (first element only)
**Example:**
```r
x <- c(TRUE, FALSE, TRUE)  
y <- c(TRUE, TRUE, FALSE)
x && y # TRUE because only check x[1] & y[1]
```

## `Identical()`
checks whether two objects are **exactly the same in every detail**. It's all or nothing which means it either returns only TRUE or FALSE.
**Usage example**
```R
identical(x, y) # TRUE or FALSE
```