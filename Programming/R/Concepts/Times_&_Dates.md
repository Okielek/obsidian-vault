## Packages
* lubrdate
* zoo
* xts
## `Sys.Date()`
Returns the current date. In a format of `"RRRR-MM-DD"` with a object of type `Date`.
## `Sys.time`
Returns the current time. Ina format of `"RRR-MM-DD HH-MM-SS TIMEZONE"` with object of type `POSIXct`.
## `as.Date()`
Converts a string into a date.  You can specifu the format, the **default** is `"%Y-%d-%m"`.
### Usage example
```R
my_date <- as.Date("2026.04.11", format = "%Y.%m.%d")
my_date # "2026-04-11"
class(my_date) # Date
```
### Cheatsheeet
* `%Y` – 4-digit year (1982)  
* `%y` – 2-digit year (82)  
* `%m` – 2-digit month (01)  
* `%d` – 2-digit day of the month (13)  
* `%A` – weekday (Wednesday)  
* `%a` – abbreviated weekday (Wed)  
* `%B` – month (January)  
* `%b` – abbreviated month (Jan)
## `as.POSIXct()`
Converts string into a **POSIXct** datatype (specified time). Default format is 
`"%Y-%d-%m %h:%m:%s timezone"`. UTC is the default timezone
### Usage example
```R
my_time <- as.POSIXct("2026-04-11 13:46:56")
my_time # "2026.04.11 13:46:56 UTC"
```