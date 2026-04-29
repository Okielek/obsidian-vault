---
tags:
  - bash
  - programming
  - for-loop
  - if-statement
  - user-input
  - scripting
---

## Overview
Bash scripts are files containing shell commands that can be executed by Bash.

## Creating a Script

### Shebang
At the top of the file, include:

```bash
#!/usr/bin/env bash
```

This tells the system to run the script using Bash.

### Make the Script Executable
After writing the script, make it executable with:

```bash
chmod +x <script>
```

## Running a Script

### Run with Bash
You can run a script by passing it to `bash`:

```bash
bash script.sh
```

### Run as an Executable
If the script is executable and has a shebang, you can run it directly:

```bash
./script.sh
```

### Syntax Check
To check for syntax errors without executing the script:

```bash
bash -n <script>
```

## File Extension
A Bash script does not need a `.sh` extension. The extension is optional and mainly helps with readability and organization.

## Commands

### `read`
Used to read user input.
#### Example
```bash
read -p "Enter your name: " name
```

This stores the user's input in the variable `$name`.

## Loops

### `for` Loop
You can loop over a list using a `for` loop.
#### Syntax
```bash
for thing in list; do
  <command>
done
```

---


## `if` statements
It checks whether condition is met and if it is it executes code after`\t`. 
To close an if statement use `fi`.
#### Syntax
```bash
if condition; then
	code
fi
```