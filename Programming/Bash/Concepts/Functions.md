---
tags:
  - functions
  - bash
  - scripting
  - programming
---

## Info 
Fucntions in bash should be though as mini programs.

## Defining a function

### Syntax
```
function() {
	execute
}
```
### Example
```bash
greet() {
	local name=$1
	echo "hello $name"
	return 0is there
}

for name in "@"; do
	greet "$name"
done
```