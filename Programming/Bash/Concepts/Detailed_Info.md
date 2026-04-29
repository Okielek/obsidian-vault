---
tags:
  - bash
  - echo
  - grep
  - ls
  - rm
  - cd
  - programming
---

## `rm` 
### Important flags
* `-i` — interactive (asks before deleting)
* `-r` — recursive (for directories)
* `-f` — force (no prompts)
* `-rf` — force and recursive **dangerous!** 
## `ls`
### Important flags
* `-a` — shows all files (including hidden such as *.file.txt*)
* `-l` — long listing, shows more info about files
## `cd`
### Important flags
* `-` — last open directory
## `grep`
### Important flags
* `-A<int>` — prints matched line and `<int>` ammount of lines **after** it.
* `-B<int>` — prints matched line and `<int>` ammount of lines **before** it.
* `-C<int>` — prints matched line and `<int>` ammount of lines **before** and  **after** it. 
* `-i` — case sensitively means (grep **a** also searches for **A**)
* `-o` — only print the parts that match the pattern (it usually prints the whole line)
### Compatible with
* [[Regular_Expressions]] (for text manipulation)

## `echo` 
### Important flags
* `>` — redirects to a file and **overwrites** it.
	 * `echo <input> > <file>`
* `>>` — redirects to a file and **appends** to it it. (It appends it to a new line )
	 *  `echo <input> >> <file>`