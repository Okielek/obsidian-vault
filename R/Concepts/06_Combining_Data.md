### `cbind()/rbind()`
Merges matrixes by column/row.
**Usage Example:**
```r
my_matrix <- matrix(vector, nrow = 3, byrow = TRUE, dimnames = list)
sum_matrix <- rowSums(my_matrix)
all_matrix <- cbind(my_matrix, sum_matrix)
```
