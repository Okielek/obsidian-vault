---
tags:
  - regex
  - programming
  - text-manipulation
  - logic-symbols
---


## What is regex?
A **regular expression** is a pattern used to match text (strings).  
Used across many languages (R, Python, JS, Bash, etc.).

---

## Core idea
You describe *what a string should look like*, not the exact string.

---

## Most important patterns

### Anchors (position)
- `^text` → starts with "text"  
- `text$` → ends with "text"  
- `^text$` → exact match "text"  

---

### Basic matching
- `text` → contains "text"  
- `.` → any single character  
- `.*` → any sequence of characters  

---

### Character sets
- `[abc]` → any of: a, b, c  
- `[a-z]` → any lowercase letter  
- `[A-Z]` → any uppercase letter  
- `[0-9]` → any digit  

---

### Predefined classes *(not always enabled by default)*
- `\d` → digit  
- `\s` → whitespace  
- `\w` → word character (letters, digits, `_`)  

⚠️ In some languages (e.g. R), you may need special flags (like `perl=TRUE`) or escape `\\d`.

---

### Logic
- `a|b` → OR (matches "a" or "b")  

---

### Quantifiers (how many times)
- `a*` → 0 or more of "a"  
- `a+` → 1 or more of "a"  
- `a?` → 0 or 1 of "a"  
- `a{3}` → exactly 3 times  
- `a{2,5}` → between 2 and 5 times  

---

## Examples (language-agnostic)

- `^a` → starts with "a"  
- `e$` → ends with "e"  
- `a.*e` → "a" followed later by "e"  
- `^(cat|dog)` → starts with "cat" or "dog"  
- `[0-9]+` → one or more digits  

---

## Common use cases

- Validate input (emails, numbers, IDs)  
- Search/filter text  
- Replace patterns  
- Extract parts of strings  

---

## ⚠️ Important notes

- Regex is **not the default in all functions/languages**  
- Special characters often need escaping (`\\` vs `\`)  
- Simpler functions like `startsWith()` may be better for basic checks  

---

## Mental model

- `^` → beginning  
- `$` → end  
- `.` → anything  
- `*` → repeat  

👉 Combine these to describe patterns instead of exact text