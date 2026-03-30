Commands in Base **R**.
### `dir():`
* show current  working directory
### `lapply():`
* creates a list and applies anything we want to all elements of the list
### `library():`
* loads in library
### `glimpse()`
shows some basic data about the dataset
### `summary()`
Gives you a quick overview of the contents of a variable.
### `c()`
initialize a vector in R. 
#### additional info:
1. If you add v1 to v2 it will add like in numpy i mean it will do `new_v[i] = v1[i] + v2[i]` for each i. The same goes for any logical operation like: "-, *, ^, >, ="
```
v1 -> [1, 2, 3, 4]; v2 -> [T, F, T, F] 
v3 -> v1[v2]                            # v3 = [1, 3]
```
1. `sum(vector)` returns the sum of the whole vector.
### `names()`
You can use it on a list to create dictionary. The dictionray works just like in python
**Usage example:**
```
list <- c(1, 2, 3)
names(list) <- c("a", "b", "c")
list["a"]
```
this will print out 1.

### `mean()`
returns the average of a vector.
### `matrix()`
Used to construct a 2D array containing only one data type.
**Usage example:**
1.  Initializing a matrix:
```
matrix(1:9, byrow = TRUE, nrow = 3) #this gives:
								#	1 2 3
								#	4 5 6
								#	7 8 9
```
2. Getting specific rows/columns
```
matrix # (from prev example)
matrix[1:2, 1:2] # this will result in a matrix: 
											#  1 2
											#  4 5
```
### `colnames()/rownames()`
You can use these commands to name columns/row in matrixes just like u could with vectors.
### `rowSums()`
Used to calculate the sum of each row in a matrix.
**Usage Example:**
```
my_matrix <- matrix(1:9, nrows = 3)
sum_matrix <- row_sums(my_matrix)
```
### `cbind()/rbind()`
Merges matrixes by column/row.
**Usage Example:**
```
my_matrix <- matrix(vector, nrow = 3, byrow = TRUE, dimnames = list)
sum_matrix <- rowSums(my_matrix)
all_matrix <- cbind(my_matrix, sum_matrix)
```
### `ls():`
Let's you check the contents of your workspace.
### `factor():`
You use this command to initialize factor factor is basically is our way of saying to or this variable will have a limited number of options f.e Sex: Male or Female.
**Usage Example:**
```
temperature_vector <- c("High", "Low", "High","Low", "Medium")
factor_temperature_vector <- factor(temperature_vector, order = TRUE, levels = c("Low", "Medium", "High"))
factor_temperature_vector # Low < Medium < High
```
by using order = TRUE and then providing levels = vector we basically initialize a way of camparing the variables with each other.
### `levels():`
Suppose we initialize a factor with c("M", "F") and we want to change it back to C("Male", "Female") thats what this is exactly for.
**Usage Example**:
```
survey_vector <- c("M", "F", "F", "M", "M")
factor_survey_vector <- factor(survey_vector)
levels(factor_survey_vector) <- c("Female", "Male")
```
