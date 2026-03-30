Part of the **tidyverse** colection, specializes in **data manipulation**.

### `%>%`
dplyr syntax known as pipe operator.
**Usage example:**
```
dataset %>%
	dplyr_command
```
### `select()`
extracts only particular variables from the dataset.
**Usage examples**
1. Select specific columns
```
dataset %>%
	select(col_name_1, col_name_2, ... , col_name_n) 
```
2. Select everything except a specific column
```
dataset %>%
	select(-col_name)
```
3. Select range of columns
```
dataset %>%
	select(col_name1:col_name_n)
```
4. Select columns that contain "string"
```
dataset %>%
	select(contains("string"))
```
#### `helpers`
?select_helpers
1. **starts/ends_with()** find columns starting/ending with a string
2. **last_col()** gets the last column
3. **matches()** select columns with specific patter

### `arrange()`
Sorts your data based on one or more variables.
**Usage example**
```
dataset %>%
	arrange(desc(variable))
```
it arranges dataset by variable in descending order.
### `filter()`
Extract observation based on given conditions.
**Usage example**
1.  basic filter usage
```
dataset %>%
	arrange(variable) %>%
	filter(condition_1, condition_2)
```
2.  filter for multiple values
```
dataset %>%
	filter(column %in% c(str_1, str_2))
```
### `mutate()`
add new variables or change existing ones
**Usage example:**
```
dataset %>%
	mutate(new_variable = f(x) )
```
u can also use it as a select and mutation in one.
```
dataset %>%
	mutate(variable_1, variable_2, ..., variable_n 
	new_variable = f(x), .keep = "none" )
```
.keep = "none" specifies that we keep only the variables stated in mutate().
### `count()`
count the number of observations.
**Usage example:**
```
dataset %>%
	count(column, wt = variable, sort = True)
```
wt stands for weight and by using it we specify what exactly we want to count. 
### `summarize()`
takes many observation and makes them into one.
**Usage example:**
```
dataset %>%
	summarize(new_variable_1 = f(x),
			  new_variable_2 = g(x) )
```
functions often used inside summarize: sum(), mean(), median(), min(), max(), n()
### `group_by()`
Groups the whole database by selected columns. 
**Usage example:**
```
dataset %>%
	group_by(column1, column2, ... , column_n)
```
### `slice_min/max()`
allows us to extract the most extreme observation form each group
**Usage example:**
```
dataset %>%
	group_by(column) %>%
	slice_max(variable, n = 1)
```
it returns only the variable thats the highest
### `rename()`
renames a column_name
**Usage example:**
```
dataset %>%
	rename(new_name = old_name)
```
we can just specify this in select instead.
### `relocate()`
used for changing column position quickly and efficiently.
**Usage example:**
```
dataset %>%
	relocate(column_name_1, .before/.after = column_name_2)
```
this relocates column_1 before/after column_2
### `lag()`
moves each item in the vector by one to the right
**Usage example:**
suppose we have a popularity meter of items for each year. Then if we want to see the trend of popularity we use lag().
```
dataset %>%
	arrange(year) %>%
	mutate(difference = popularity - lag(popularity))
```