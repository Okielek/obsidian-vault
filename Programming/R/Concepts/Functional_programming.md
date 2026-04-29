---
tags:
  - programming
  - R
  - apply
---

## `lapply()`
Creates a list and applies anything we want to all elements of the list. **ALWAYS RETURNS A LIST**
### Usage example:
```R
list <- list(x = 420, c("a", "b", "c"), logical = TRUE)
lapply(list, class) # "numeric", "character", "logical"
```
## `sapply()`
Works just like lapply but converts the list into an **array**/**vector**. However if converting the output into an array is not possible it behaves just like laplly and returns a list.
## `vapply()`
Works just like lapply but converts the list into **specified datatype**. If its not possible to conver data into the **specified datatype** it will return an error.
### **Usage example**
```R
cities <- c("New York", "Paris", "London")
vapply(cities, nchar, numeric(1)) # 8, 5, 6
```

