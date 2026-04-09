## `paste()`
Prints the output of whats inside the brackets however works more like an f"string in py. Automatically puts spaces between , if you want to avoid this use: `paste0()`. ^paste
### Usage example
```r
age <- 20
paste("I am", age, "years old") # I am age years old
```
## `paste0()`
Works just like [[11_String_Manipulation#^paste|paste()]]  but doesn't add spaces automatically it is superior. ^paste0
### Usage example
```r
number <- 6969
paste0("mariuszek", number, "xd") # mariuszek6969xd

```
## `tolower()`
Converts string into lowercase string.