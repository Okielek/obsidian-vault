---
tags:
  - variables
  - bash
  - programming
---

## How to use?
* To **use** a *variable* in bash you have to put `$` before a it.
	* usg ex: `echo $PATH 
* To **initialize** a variable just use `=`.
	* usg ex: `name=jakub`
* To **get rid of** variable use `unset`.
* to **execute a command** in another command use `$( )`
## Built in variables
* `$PATH` — path which is checked when giving any command in bash
* `$PWD` — current working directory
* `$USER` — user that's logged in
* `$SHELL` — the shell you are running (bash version)
* `$HOSTNAME` — host name of your machine
* `$MACHTYPE` — returns type of machine system is running on
* `$?` — exit code of last run command
* `$1` — first positional argument passed to a script
* `$n` — n-th positional argument passed to a script
* `$@` — array of all of the arguments passed to a script