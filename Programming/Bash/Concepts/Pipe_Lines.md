---
tags:
  - bash
  - pipe-lines
  - programming
---

### Concept
A pipeline passes the output (stdout) of one command as input (stdin) to another.

command1 | command2

---

### Mental model
Think of it like a stream:
[data] → cmd1 → cmd2 → cmd3 → result

Each command should:
- take input from stdin
- output to stdout

---

### Basic examples

#### Filter text
cat file.txt | grep "error"

#### Count lines
cat file.txt | wc -l

#### Sort + unique
cat file.txt | sort | uniq

---

### Common tools (MOST IMPORTANT)

- grep → filter
- sort → sort lines
- uniq → remove duplicates
- wc → count
- cut → extract columns
- awk → process structured text
- tr → replace characters

---

### Real examples

#### Count unique IPs
cat access.log | cut -d' ' -f1 | sort | uniq -c | sort -nr

#### Find largest files
ls -lh | sort -k5 -hr

---

### Tips

- Avoid useless use of cat:
  ❌ cat file.txt | grep "x"
  ✅ grep "x" file.txt

- Use pipes when chaining transformations

---

### Advanced

#### Redirect stderr
command1 2>&1 | command2

#### Save output
command1 | tee output.txt

#### Parallel thinking
Each step transforms data

---

### Cheatsheet

| Task | Pipeline |
|------|--------|
| count lines | wc -l |
| filter | grep |
| unique | sort \| uniq |
| columns | cut -d',' -f1 |
