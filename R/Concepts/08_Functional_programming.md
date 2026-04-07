### `lapply()`
* Creates a list and applies anything we want to all elements of the list. **ALWAYS RETURNS A LIST**
### Usage example:
```R
list <- list(x = 420, c("a", "b", "c"), logical = TRUE)
lapply(list, class) # "numeric", "character", "logical"
```
