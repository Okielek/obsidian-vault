---
tags:
  - R
  - data-manipluation
  - programming
  - cbind
  - append
---


### `cbind()/rbind()`
Merges matrixes by column/row.
**Usage Example:**
```r
my_matrix <- matrix(vector, nrow = 3, byrow = TRUE, dimnames = list)
sum_matrix <- rowSums(my_matrix)
all_matrix <- cbind(my_matrix, sum_matrix)
```
## `append()`
Adds element to a vector, by default it adds it to the end of the list.
### Usage example
```R
append(element, vector) # c(...., element)
append(1, c(0, 2, 3), after=1) # 0, 1, 2, 3
```
