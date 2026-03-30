### `names()`
You can use it on a list to create dictionary. The dictionray works just like in python
**Usage example:**
```r
list <- c(1, 2, 3)
names(list) <- c("a", "b", "c")
list["a"]
```
this will print out 1.


### `colnames()/rownames()`
You can use these commands to name columns/row in matrixes just like u could with vectors.

### `levels()`
Suppose we initialize a factor with c("M", "F") and we want to change it back to C("Male", "Female") thats what this is exactly for.
**Usage Example**:
```r
survey_vector <- c("M", "F", "F", "M", "M")
factor_survey_vector <- factor(survey_vector)
levels(factor_survey_vector) <- c("Female", "Male")
```
