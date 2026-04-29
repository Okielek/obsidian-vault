---
tags:
  - bash
  - cheatsheet
  - important
  - programming
---



### Info
Bash always exists in some directory!

### Basic Commands
* `echo` — prints out the content back to the terminal
	* Usage: `echo <input>`
	* See: [[Detailed_Info#`echo`|details]]
* `cd` — change directory
	* Usage: `cd <directory>`
* `pwd` — print working directory
* `ls` — list all files
	* See: [[Detailed_Info#`ls`|details]]
* `touch` — creates a file
* `rm` — removes file
	* Usage: `rm <file>`
	* See: [[Detailed_Info#`rm`|details]]
* `clear` — clears the terminal (CTRL+L)
* `mkdir` — makes a directory
	* Usage: `mkdir <directory>`
* `history` — prints terminal history
* `type` — gives you the type of a command (can be built-in or not)
* `file` — gives you the type of a specified file
* `chsh` — changes a users shell
* `uniq` — returns only unique outputs
* `wc` — counts words (stands for word count)
### Files
#### File Manipulation
* `mv` — moves the file from *file1* to *file2*. It **overwrites** a file! Can be used to **rename** a file.
	* Usage: `mv <file1> <file2>`
* `cp` — copies *file1* to *file2*. It **overwrites**.

#### File Searching
* `cat` — prints the contents of a *file*.
* `less` — prints out the content of a *file* but paginates data.
* `grep` — searches a file/input for a specified pattern and prints it out.
	* Usage: `grep <pattern> <file>`
	* See: [[Detailed_Info#`grep`|details]]
* `which` — prints out the directory of a given file.

### Strings
#### String Manipulation
* `tr` — translates, **replaces** *var1* with *var2* within text.
	* Usage: `echo $PATH | tr : "\n"` 
* `cut` — shows only a specific part of a .*text* file
	* usage: `cat file.csv | cut -d, -f 1` (first column)
* `sed` — basic find and replace
	* usage: `sed 's#to_replace#replacement#'`
* `awk` — no idea seems really complicated #tolearn

### Scripts
* `#!/usr/bin/env bash` — use at the top of the file.
* `chmod +x` — converts a file into an executable file.
