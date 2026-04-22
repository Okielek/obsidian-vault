# ggplot2
## `ggplot()`
standard way to plot
**Usage example:**
```
ggplot(database, aes(x = var_1, y = var_2)) + 
	   geom_line() 
```
## `aes()
You can specify a lot of variables inside of `ggplot()` that can adjust how the final chart looks.
* `x` $-$ specifies the variable for the **x-axis**. (must specify)
* `y` $-$ specifies the variable for the **y-axis**. (must specify)
* `color` $-$ specifies the color (can be assigned to df column to sort by color)
* `size` $-$ specifies the size
* `shape` $-$ specifies the shape
* `fill` $-$ as in fill color

## plot types
* `geom_point()` $-$ adds points (as in scatter plot)
* `geom_smooth()` $-$ adds a smooth tend curve

**Usage example**
```
ggplot(data,aes(x,y)) +
	geom_point()
```
## `geom_*()`
Variables to specify inside the `geom_*()` functions.
* `alpha()` $-$ controls the opacity of a plot values between ($0 - 1$) with 0 being fully opate