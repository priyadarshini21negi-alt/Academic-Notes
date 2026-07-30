
---
# Regex + grep Cheatsheet

## What is Regex?

> A **Regular Expression (Regex)** is a pattern used to search, filter, or match text.

Most common use:

```bash
grep 'pattern' file.txt
```

or

```bash
cat file.txt | grep 'pattern'
```

---

# grep Basics

```bash
grep 'pattern' file
```

- Searches **line by line**
    
- Prints only matching lines
    
- Always use **single quotes** around regex.
    

```bash
grep 'hello' file.txt
```

---

# BRE vs ERE

## BRE (Basic Regular Expression)

Default `grep`

```bash
grep 'pattern' file
```

Needs escaping:

```text
\( \)
\{ \}
```

---

## ERE (Extended Regular Expression)

```bash
egrep 'pattern' file
```

or

```bash
grep -E 'pattern' file
```

No escaping needed:

```text
()
{}
+
?
|
```

---

# Regex Special Characters

|Symbol|Meaning|
|---|---|
|`.`|Any one character|
|`*`|0 or more of previous character|
|`+`|1 or more (ERE only)|
|`?`|0 or 1 (ERE only)|
|`[]`|Character set|
|`[^ ]`|NOT these characters|
|`-`|Range inside `[]`|
|`^`|Beginning of line|
|`$`|End of line|
|`\`|Escape special character|
|`\b`|Word boundary|

---

# Character Classes

Instead of writing long ranges.

Examples:

```text
[:digit:]
[:alpha:]
[:alnum:]
[:space:]
[:lower:]
[:upper:]
[:punct:]
[:print:]
```

Used like

```regex
[[:digit:]]
```

---

# Important Patterns

## Match any character

```regex
.
```

Matches

```
cat
cut
cot
```

---

## Match zero or more

```regex
ab*
```

Matches

```
a
ab
abb
abbb
```

---

## Match one or more (ERE)

```regex
ab+
```

Matches

```
ab
abb
abbb
```

Not

```
a
```

---

## Beginning of line

```regex
^hello
```

Only matches

```
hello world
```

Not

```
say hello
```

---

## End of line

```regex
world$
```

Matches only if line ends with

```
world
```

---

## Literal dot

Normally

```regex
.
```

means "any character"

To match an actual period:

```regex
\.
```

---

## Word Boundary

```regex
am\b
```

Matches

```
I am
```

Not

```
amazon
```

---

# Character Sets

## One of these characters

```regex
[abc]
```

Matches

```
a
b
c
```

---

## Range

```regex
[1-5]
```

Same as

```
12345
```

---

## Negation

```regex
[^1-5]
```

Matches anything except

```
1 2 3 4 5
```

---

# Repetition

Exactly 2

```regex
M\{2\}
```

Between 2 and 4

```regex
M\{2,4\}
```

In BRE:

```text
\{ \}
```

In ERE:

```text
{}
```

---

# Grouping

BRE

```regex
\(ab\)
```

ERE

```regex
(ab)
```

Useful when repeating whole patterns instead of one character.

---

# Back References

Save a matched group.

```
(group)\1
```

`\1` = first group

`\2` = second group

...

`\9`

Example

```regex
\(ma\).*\1
```

Matches

```
ma......ma
```

---

# Alternation (OR)

Only in ERE

```regex
(cat|dog)
```

Matches either

```
cat
```

or

```
dog
```

---

# Operator Meaning

## `M*`

Means

```
zero or more M
```

NOT

```
anything after M
```

---

## `M.*a`

Means

```
M
(any characters)
a
```

This is what people usually want.

---

# Common grep Patterns

## Search text

```bash
grep 'hello' file
```

---

## Pipe into grep

```bash
cat file | grep 'hello'
```

---

## Dot

```bash
grep 'S.n'
```

Matches

```
Sin
San
Sun
```

---

## End of line

```bash
grep 'am$'
```

---

## Literal period

```bash
grep '\.'
```

---

## Beginning of line

```bash
grep '^M'
```

---

## Word boundary

```bash
grep 'am\b'
```

---

## Character choice

```bash
grep 'M[ME]'
```

Matches

```
MM
ME
```

---

## Character range

```bash
grep '[1-5]'
```

---

## Negated range

```bash
grep '[^1-5]'
```

---

## Repetition

```bash
grep 'M\{2,4\}'
```

---

## Back reference

```bash
grep '\(ma\).*\1'
```

---

## Repeat grouped pattern

```bash
grep '\(ab\)\{2,3\}'
```

---

## One or more (ERE)

```bash
egrep 'M+'
```

---

## Beginning + one or more

```bash
egrep '^M+'
```

---

## Beginning + zero or more

```bash
egrep '^M*'
```

---

## Difference

```bash
egrep 'M*a'
```

=

```
zero or more M
then a
```

Whereas

```bash
egrep 'M.*a'
```

=

```
M
anything
a
```

---

## Repeat group

```bash
egrep '(ma)+'
```

---

## Zero or more groups

```bash
egrep '(ma)*'
```

---

## OR

```bash
egrep '(ED|ME)'
```

---

# ⭐ Must Remember (Exam/Fast Recall)

- Regex = **text pattern matching**
    
- `grep` → Basic Regex (BRE)
    
- `egrep` / `grep -E` → Extended Regex (ERE)
    
- `.` = any character
    
- `*` = 0 or more
    
- `+` = 1 or more (ERE)
    
- `[]` = choose one character
    
- `[^ ]` = not these characters
    
- `^` = start of line
    
- `$` = end of line
    
- `\b` = word boundary
    
- `\.` = literal `.`
    
- `()` = group
    
- `\1` = first matched group
    
- `|` = OR (ERE)
    
- `M*` ≠ `M.*`
    
    - `M*` → zero or more `M`
        
    - `M.*` → `M` followed by anything