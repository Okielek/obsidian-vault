---
tags:
  - R
  - data-visualization
  - ggplot2
  - plotting
  - programming
---

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
	* sg ex: `ggplot(aes()) + geom_point(size=4)`
* `shape` $-$ specifies the shape
	* usg ex: `ggplot(aes()) + geom_point(shape=1)`
* `fill` $-$ as in fill color
* `position` — position of values on the plot
	* default is `position="identity"` which means the data will apear exactly in its corresponding values.
	* if there are a lot of overlapping values you can use `"jitter"` which will add some noise to the values making them visible.

## plot types
* `geom_point()` — adds points (as in scatter plot)
* `geom_smooth()` — adds a smooth tend curve
* `geom_text()` — adds a scatter plot put with text instead of dots

**Usage example**
```
ggplot(data,aes(x,y)) +
	geom_point()
```
## `geom_*()`
Variables to specify inside the `geom_*()` functions.
* `alpha()` $-$ controls the opacity of a plot values between ($0 - 1$) with 0 being fully opate
## Scale functions
- `scale_x_*()`
- `scale_y_*()`
- `scale_color_*()`
  - Also `scale_colour_*()`
- `scale_fill_*()`
- `scale_shape_*()`
- `scale_linetype_*()`
- `scale_size_*()`

Replace `*` depending on data type:  
- `continuous` → numeric data  
- `discrete` → categorical data (factors/strings)  
- `date`, `datetime` → time data
### Arguments
You can specify arguments in scale functions. First one is always the name of the scale.
- `limits` — describe the scales range
- `breaks` — control the tickmark positions
- `expand` — takes in a vector of length 2 and creates a gap between the x and y axis and the start of the values appearing.
- `labels` — adjust the category names
#### Usage Example:
```R
ggplot(iris, aes(x = Sepal.Length,
                 y = Sepal.Width,
                 color = Species)) +
  geom_point(position = "jitter") +
  scale_x_continuous("Sepal Length",
                     limits = c(2, 8),
                     breaks = seq(2, 8, 3),
                     expand = c(0, 0),
                     labels = c("Setosa",
                                "Versicolor",
                                "Virginica")) +
  scale_color_discrete("Species")
```
  

## Some plot examples
1) Difference between color and fill
```R
ggplot(mtcars, aes(wt, mpg, fill = fcyl, color=fam)) +
	geom_point(shape = 21, size = 4, alpha=0.6)
```