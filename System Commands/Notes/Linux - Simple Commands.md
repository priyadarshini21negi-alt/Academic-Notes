
---
# Linux File System Basics

Linux organizes everything in a hierarchical directory structure.
The topmost directory is called the **root directory**:
```bash
/
```
Everything starts from here.

---
# Important Directory Shortcuts

| Symbol | Meaning            |
| ------ | ------------------ |
| `.`    | Current directory  |
| `..`   | Parent directory   |
| `~`    | Home directory     |
| `-`    | Previous directory |

Examples:
```bash
cd ..
cd ~
cd -
cd
```

---
# Date and Time

```bash
# Current Date and Time
date

# RFC 5322 email format. 
date -R
```

---
# Calendar

```bash
# Current month
cal

# Specific month
cal 8 1947
cal August 1947

# Vertical Calender 
ncal
```

---

# Memory Information

```bash
# Memory statistics
free

# Human readable output :-
free -h
```

---
## Swap Memory

- RAM = Fast
    
- Swap = Slow (disk-based backup memory)
    

---

# User Groups

```bash
groups
```

Displays groups of current user.

---

# Directory Listing

```bash
# Basic Listing
ls

# Long Listing 
ls -l
```
---
# Understanding ls -l

Example:

```text
drwxr-xr-x
```

### File Types

|Symbol|Meaning|
|---|---|
|`-`|Regular file|
|`d`|Directory|
|`l`|Symbolic link|
|`c`|Character device|
|`b`|Block device|
|`s`|Socket|
|`p`|Named pipe|

### Permissions

```text
rwxr-xr-x
```

Split into:

```text
rwx | r-x | r-x
```

Owner | Group | Others

---

# Permission Meaning

|Symbol|Meaning|
|---|---|
|r|Read|
|w|Write|
|x|Execute|

---

# Permission Categories

## Owner

User who owns the file.

## Group

Users belonging to the file's group.

## Others

Everyone else.

---

# Numeric Permissions

|Permission|Number|
|---|---|
|rwx|7|
|rw-|6|
|r-x|5|
|r--|4|

Common:

```text
700 → rwx------
755 → rwxr-xr-x
644 → rw-r--r--
```

---

# Changing Permissions

## Symbolic Mode

```bash
chmod g-w file
chmod g-x file
chmod o-x file
chmod o+r file
```

## Numeric Mode

```bash
chmod 700 file
```

---

# Creating Directories

```bash
mkdir dir
```

---

# Creating Files

```bash
touch file
```

Creates empty file.

Updates timestamp if file already exists.

---

# Copying Files

```bash
cp file1 file2
```

---

# Moving Files

```bash
mv file ..
```

Move file.

```bash
mv oldname newname
```

Rename file.

---

# Filenames With Spaces

```bash
mv file1 "file one"
```

---

# Deleting Files

```bash
rm file
```

Interactive mode:

```bash
rm -i file
```

---

# Aliases
An **alias** is simply a **shortcut name for another command**.
Instead of typing a long command every time, you create a shorter nickname.

# Example

Suppose you frequently use:

```
ls -l
```

You can create an alias:

```
alias ll='ls -l'
```

Now typing:

```
ll
```

is exactly the same as typing:

```
ls -l
```

Create:

```bash
# Creating an alias
alias ll='ls -l'

# Removing an alias 
unalias ll

# Common safety alias
alias rm='rm -i'
```

View:

```bash
alias
```

Remove:

```bash
unalias ll
```

Common safety alias:

```bash
alias rm='rm -i'
```

---

# Inodes

Every file has an inode.

Stores:

- Permissions
    
- Ownership
    
- Timestamps
    
- Disk location
    

View:

```bash
ls -i
ls -li
```

---

# Hard Links

Same inode:

```text
file1
file3
```

Same actual file.

---

# Hard Link Count

In:

```bash
ls -l
```

the number after permissions represents hard links.

---

# Reading Files

## less

```bash
less file.txt
```

Best text viewer.

Quit:

```text
q
```

---

## cat

```bash
cat file.txt
```

Prints entire file.

---

## more

```bash
more file.txt
```

Older pager.

> less is more

---

## head

```bash
head file.txt
head -n 5 file.txt
```

---

## tail

```bash
tail file.txt
tail -n 5 file.txt
```

---

# Counting Content

```bash
wc file.txt
```

Shows:

- Lines
    
- Words
    
- Bytes
    

Only lines:

```bash
wc -l file.txt
```

---

# Finding Commands

## Location

```bash
which command
```

---

## Short Description

```bash
whatis command
```

---

## Full Documentation

```bash
man command
```

---

## Search Commands

```bash
apropos keyword
```

Equivalent:

```bash
man -k keyword
```

---

# Bash Help

```bash
help
```

Help for shell built-ins.

---

# Info Browser

```bash
info
```

Interactive documentation browser.

---

# Command Types

```bash
type command
```

Shows whether command is:

- Alias
    
- Built-in
    
- Executable
    

---

# File Type Detection

```bash
file filename
```

Examples:

- ASCII text
    
- Binary executable
    
- Directory
    
- Symbolic link
    

---

# Text vs Binary Files

## Text

Human-readable.

Examples:

- Source code
    
- Shell scripts
    
- Config files
    

## Binary

Machine-readable.

Examples:

- Chrome
    
- VS Code
    
- Zoom
    

---

# Tab Completion

```bash
alt<TAB>
```

Auto-completes filenames.

---

# Current User

```bash
whoami
```

Displays current username.

---

# Root Directory Facts

Multiple slashes are equivalent:

```bash
/usr/bin
////usr////bin
```

---

## Root Is Its Own Parent

```bash
cd /
cd ..
```

Still remains:

```bash
/
```

---

# Advanced ls

Directory contents:

```bash
ls -l dir
```

Directory itself:

```bash
ls -ld dir
```

---

# Combining Options

```bash
ls -ldi
```

Equivalent to:

```bash
ls -l -d -i
```

---

# Long Options

Examples:

```bash
ls --inode
ls --directory
```

---

# Options vs Arguments

Option:

```bash
ls -l
```

Argument:

```bash
ls file.txt
```

---

# Multiple Arguments

```bash
touch file1 file2 file3
```

---

# Recursive Operations

## Copy Directory

```bash
cp -r dir1 dir2
```

## Delete Directory

```bash
rm -r dir1
```

---

# mv vs cp

## mv

Works on directories automatically.

```bash
mv dir1 dir2
```

## cp

Requires recursion.

```bash
cp -r dir1 dir2
```

---

# Links

## Symbolic Link

```bash
ln -s file1 file2
```

Acts like shortcut.

Different inode.

---

## Hard Link

```bash
ln file1 file3
```

Same inode.

---

# Hard Link vs Symbolic Link

|Feature|Hard Link|Symbolic Link|
|---|---|---|
|Shares inode|Yes|No|
|Separate file|No|Yes|
|Survives original deletion|Yes|No|
|Command|`ln`|`ln -s`|

---

# File Information

## stat

```bash
stat file
```

Shows:

- Size
    
- Inode
    
- Permissions
    
- Timestamps
    

---

## du

```bash
du file
du -h file
```

Disk usage.

---

# File Size vs Disk Usage

Files occupy blocks.

Typical block:

```text
4096 bytes
```

Disk usage may be larger than actual file size.

---

# Virtual Filesystems

## /proc

Kernel-generated information.

Not stored on disk.

Examples:

```bash
/proc/cpuinfo
/proc/meminfo
/proc/version
/proc/partitions
```

---

## Process IDs

Inside `/proc`:

```text
/proc/1
/proc/245
/proc/1834
```

Directories named with Process IDs (PIDs).

---

## System Information

CPU:

```bash
cat /proc/cpuinfo
```

Memory:

```bash
cat /proc/meminfo
```

Kernel:

```bash
cat /proc/version
uname -a
```

Partitions:

```bash
cat /proc/partitions
```

---

# Disk Usage

```bash
df
df -h
```

Shows:

- Filesystems
    
- Used space
    
- Free space
    
- Mount points
    

---

# /sys Filesystem

Modern hardware information interface.

Examples:

```bash
/sys/bus/usb/devices
```

Contains device information.

Examples:

```bash
cat manufacturer
cat product
```

---

# Permission Denied

Occurs when:

- No read permission
    
- No write permission
    
- No execute permission
    
- User is not owner
    

Linux uses permissions to protect system files.