## `paste()`
Prints the output of whats inside the brackets however works more like an f"string in py. Automatically puts spaces between , if you want to avoid this use: `paste0()`. ^paste
### Usage example
```r
age <- 20
paste("I am", age, "years old") # I am age years old
```
## `paste0()`
Works just like [[String_Manipulation#^paste|paste()]]  but doesn't add spaces automatically it is superior. ^paste0
### Usage example
```r
number <- 6969
paste0("mariuszek", number, "xd") # mariuszek6969xd

```
## `tolower()`
Converts string into lowercase string.

# regular expressions

## `Regex cheatsheet`
### Related functions
* `sub()` $-$ replace first match 
* `gsub() `$-$ replace all matches  
* `grep()` $-$ return indices  
* `grepl()` $-$ return TRUE/FALSE

### Most important patterns

- `^text` → starts with "text"
- `text$` → ends with "text"
- `text` → contains "text"
- `^text$` → exact match "text"
- `.` → any single character
- `.*` → any sequence of characters
- `[abc]` → any of a, b, or c
- `[a-z]` → any lowercase letter
- `[0-9]` → any digit
- `|` → OR (e.g. "cat|dog")
- `\\d` → digit (use `perl=TRUE`)
- `\\s` → whitespace (use `perl=TRUE`)

#### Examples (what actually happens)

```r
library(dplyr)

df <- data.frame(name = c("apple", "banana", "apricot", "grape", "apple123"))

# Starts with "a"
df %>% filter(grepl("^a", name))
# "apple", "apricot", "apple123"

# Ends with "e"
df %>% filter(grepl("e$", name))
# "apple", "grape"

# Contains "an"
df %>% filter(grepl("an", name))
# "banana"

# Exact match "apple"
df %>% filter(grepl("^apple$", name))
# "apple"

# Contains digit
df %>% filter(grepl("[0-9]", name))
# "apple123"

# Starts with "a" OR "b"
df %>% filter(grepl("^(a|b)", name))
# "apple", "banana", "apricot", "apple123"

# Does NOT start with "a"
df %>% filter(!grepl("^a", name))
# "banana", "grape"

# Any characters between a and e
df %>% filter(grepl("a.*e", name))
# "apple", "grape"
```

### Quick usage pattern

```r
df %>% filter(grepl("PATTERN", column))
```

## `grep()`
Detects a specific pattern and returns the indicies that match it.
### Usage example
```R
animals <- ("cat", "dog", "chicken", "iguala")
match <- grepl(pattern="a", x=animals) # [1] 1 4
animals[match] # cat iguala
```
## `grepl()`
Detects a specific pattern and returns a TRUE/FALSE statement.
### Usage example
```R
animals <- (cat, dog, chicken)
grepl(pattern="a", x=animals) # TRUE FALSE FALSE
```
## `sub()`
Subtitues a given expression.
### Usage example
``` R
animals <- c("cat", "moose", "impala")
sub(pattern = "a", replacement = "o", x=animals) 
# "cot" "moose" "impola"
```
As u can see it replaces only the first "a" in `imapala` to replace all of the instances of "a" use `gsub()`.
**Cool usage**! Replacing the end of emails to a desired one.
```R
emails <- c("john.doe@ivyleague.edu", "education@world.gov", "global@peace.org",
			"invalid.edu", "quant@bigdatacollege.edu", "cookie.monster@sesame.tv")
sub(pattern="@.*\\.edu$", replacement="@datacamp.edu", x=emails )	
# this replaces all of the .edu ones with out replacement
# example:john.doe@ivyleague.edu -> john.doe@datacamp.edu
```
## `gsub()`
Replaces all of the instances of a given expression. 
### Usage example
``` R
animals <- c("cat", "moose", "impala")
sub(pattern = "a", replacement = "o", x=animals) 
# "cot" "moose" "impolo"
```


