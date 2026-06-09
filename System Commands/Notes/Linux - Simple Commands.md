
# Linux File System Basics

Linux organizes everything in a hierarchical directory structure.

The topmost directory is called the **root directory**:

```bash
/
```

Everything starts from here.

---

# Important Directory Shortcuts

| Symbol | Meaning |
|----------|----------|
| `.` | Current directory |
| `..` | Parent directory |
| `~` | Home directory |
| `-` | Previous directory |

---

# Viewing Date and Time

```bash
date
```
Example:
```text
Tue Jun 09 11:30:12 IST 2026
```

---

## RFC Format

```bash
date -R
```

Displays date in RFC 5322 format (used in email systems).

---

# Calendar Commands

Show current month:

```bash
cal
```

Show a specific month:

```bash
cal 8 1947
cal August 1947
```

---
## Alternative Calendar Layout

```bash
ncal
```

Displays calendar vertically.

---

# Memory Information

```bash
free
```

Shows memory statistics.

Better format:

```bash
free -h
```

Example:

```text
Total RAM : 31G
Used RAM  : 1.2G
Free RAM  : 26G
```

---

## Swap Memory

Swap is disk space used as backup memory when RAM is full.

- RAM = Fast
- Swap = Slow

High swap usage generally indicates memory pressure.

---

# User Groups

```bash
groups
```

Shows groups the current user belongs to.

Example:

```text
student sudo docker
```

If you belong to `sudo`, you have administrator privileges.

---

# Directory Listings

## Simple Listing

```bash
ls
```

---

## Long Listing

```bash
ls -l
```

Example:

```text
drwxr-xr-x 2 user group 4096 Nov 25 Documents
```

---

# Understanding ls -l Output

Example:

```text
drwxr-xr-x
```

### First Character = File Type

| Symbol | Meaning |
|----------|----------|
| `-` | Regular file |
| `d` | Directory |
| `l` | Symbolic link |
| `c` | Character device |
| `b` | Block device |
| `s` | Socket |
| `p` | Named pipe |

---

### Remaining 9 Characters = Permissions

Example:

```text
rwxr-xr-x
```

Split into groups of three:

```text
rwx | r-x | r-x
```

Owner | Group | Others

---

# Permission Meaning

| Symbol | Meaning |
|----------|----------|
| r | Read |
| w | Write |
| x | Execute |

---

# Numeric Permissions

Permission values:

| Permission | Value |
|------------|--------|
| r | 4 |
| w | 2 |
| x | 1 |

Examples:

| Permission | Number |
| ---------- | ------ |
| rwx        | 7      |
| rw-        | 6      |
| r-x        | 5      |
| r--        | 4      |

---

## Common Permission Modes

### 700

```text
rwx------
```

Owner only.

---

### 755

```text
rwxr-xr-x
```

Owner full access.

Others can read and execute.

---

### 644

```text
rw-r--r--
```

Typical file permission.

---

# Changing Permissions

## Symbolic Mode

Remove write permission from group:

```bash
chmod g-w file
```

Remove execute permission:

```bash
chmod g-x file
```

Add read permission:

```bash
chmod o+r file
```

---

## Numeric Mode

```bash
chmod 700 file
```

---

# Creating Directories

```bash
mkdir level1
```

Creates directory.

---

# Creating Files

```bash
touch file1
```

Creates empty file.

---

## Secondary Purpose

```bash
touch existing_file
```

Updates timestamp.

---

# Copying Files

```bash
cp file1 file2
```

Creates a copy.

---

# Moving Files

```bash
mv file2 ..
```

Moves file to parent directory.

---

# Renaming Files

```bash
mv oldname newname
```

Example:

```bash
mv file2 file2a
```

---

# Filenames With Spaces

Wrong:

```bash
mv file1 file one
```

Linux sees two separate arguments.

Correct:

```bash
mv file1 "file one"
```

---

# Deleting Files

```bash
rm file1
```

Deletes file.

---

## Safer Removal

```bash
rm -i file1
```

Prompts before deleting.

---

## Permanent Alias

```bash
alias rm='rm -i'
```

---

# Inodes

Every file has an inode.

An inode stores:

- file metadata
- permissions
- ownership
- location on disk

View inode numbers:

```bash
ls -i
```

or

```bash
ls -li
```

---

# Hard Links

Multiple filenames can point to the same inode.

Same inode:

```text
file1
file3
```

Same actual file.

---

# Reading Files

```bash
less file.txt
```

Navigate file page-by-page.

Controls:

- Space = next page
- q = quit

---

# Tab Completion

Instead of typing:

```bash
alternatives.log
```

Type:

```bash
alt<TAB>
```

Bash completes it.

---

# Determining File Type

```bash
file filename
```

Examples:

```bash
file script.sh
```

Output:

```text
ASCII text
```

---

```bash
file zoom
```

Output:

```text
symbolic link
```

---

```bash
file zoom-launcher
```

Output:

```text
ELF 64-bit executable
```

---

# ASCII vs Binary Files

## ASCII

Human-readable text.

Examples:

- Source code
- Shell scripts
- Configuration files

---

## Binary

Machine-readable.

Examples:

- Chrome
- VS Code
- Zoom

Opening them as text produces garbage.

---

# Permission Denied Errors

Occurs when:

- You are not owner
- No read permission
- No write permission
- No execute permission

Linux protects system files this way.

---

# Advanced Linux Commands

---

# Root Directory Facts

Multiple slashes are treated the same:

```bash
/usr/bin
```

is equivalent to

```bash
////usr////bin
```

---

## Root Is Its Own Parent

```bash
cd /
cd ..
```

Still remains in:

```bash
/
```

---

# Advanced ls Usage

---

## View Contents of Another Directory

```bash
ls -l level1
```

Shows contents inside level1.

---

## View Directory Itself

```bash
ls -ld level1
```

Shows information about level1 without entering it.

---

## Display Inode Number

```bash
ls -li
```

---

# Long Options

Many commands have readable forms.

Examples:

```bash
ls --inode
```

```bash
ls --directory
```

Equivalent to:

```bash
ls -i
```

```bash
ls -d
```

---

# Reading Text Files

---

## less

```bash
less file.txt
```

Best text viewer.

Supports scrolling.

---

## cat

```bash
cat file.txt
```

Prints entire file immediately.

Good for small files.

---

## more

```bash
more file.txt
```

Older pager.

Less powerful than `less`.

---

## head

First 10 lines:

```bash
head file.txt
```

Custom:

```bash
head -n 5 file.txt
```

---

## tail

Last 10 lines:

```bash
tail file.txt
```

Custom:

```bash
tail -n 5 file.txt
```

---

# Counting Lines, Words and Bytes

```bash
wc file.txt
```

Output:

```text
27 97 581 file.txt
```

Meaning:

- 27 lines
- 97 words
- 581 bytes

---

## Only Count Lines

```bash
wc -l file.txt
```

---

# Finding Commands

---

## Where Is A Command?

```bash
which ls
```

Output:

```text
/usr/bin/ls
```

---

## What Does A Command Do?

```bash
whatis ls
```

Output:

```text
ls - list directory contents
```

---

## Full Documentation

```bash
man ls
```

---

# Discovering New Commands

Search descriptions:

```bash
apropos keyword
```

Example:

```bash
apropos who
```

---

Equivalent:

```bash
man -k who
```

---

# Bash Help

```bash
help
```

Lists shell built-in commands.

---

# Info System

```bash
info
```

Interactive documentation browser.

Navigation:

- Enter = open
- Left Arrow = back

---

# Understanding type

Shows command origin.

```bash
type ls
```

Possible results:

```text
ls is aliased to ...
```

or

```text
ls is /usr/bin/ls
```

or

```text
type is a shell builtin
```

---

# Aliases

Create:

```bash
alias ll='ls -l'
```

Use:

```bash
ll
```

---

## View Aliases

```bash
alias
```

---

## Remove Alias

```bash
unalias ll
```

---

# Arguments vs Options

Option:

```bash
ls -l
```

`-l` is an option.

---

Argument:

```bash
ls file.txt
```

`file.txt` is an argument.

---

# Multiple Arguments

```bash
touch file1 file2 file3
```

Creates all files at once.

---

# Recursive Operations

---

## Copy Directory

```bash
cp -r dir1 dir2
```

Copies entire directory tree.

---

## Delete Directory

```bash
rm -r dir1
```

Deletes directory and everything inside.

---

# Hard Links vs Symbolic Links

---

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

Same actual file.

---

# File Information

---

## stat

```bash
stat file.txt
```

Shows:

- size
- permissions
- timestamps
- inode

---

## du

Disk usage:

```bash
du file.txt
```

Human readable:

```bash
du -h file.txt
```

---

# Why File Size Differs

Example:

Actual size:

```text
4553 bytes
```

Disk usage:

```text
8 KB
```

Reason:

Files occupy blocks.

Typical block:

```text
4096 bytes
```

A file larger than 4096 bytes requires two blocks.

---

# /proc Filesystem

```bash
cd /proc
```

Virtual filesystem generated by the kernel.

Not stored on disk.

---

## CPU Information

```bash
cat /proc/cpuinfo
```

---

## Memory Information

```bash
cat /proc/meminfo
```

---

## Kernel Information

```bash
cat /proc/version
```

or

```bash
uname -a
```

---

## Partition Information

```bash
cat /proc/partitions
```

---

## Disk Usage

```bash
df -h
```

Shows:

- partition size
- used space
- free space
- mount points

---

# /sys Filesystem

```bash
cd /sys
```

Provides hardware and device information.

Examples:

USB devices, drivers, buses, CPUs.

---

## USB Device Information

Manufacturer:

```bash
cat manufacturer
```

Product:

```bash
cat product
```

Useful for identifying connected hardware.

---

# Most Important Commands To Remember

```bash
pwd
cd
ls
ls -l
mkdir
touch
cp
cp -r
mv
rm
rm -r
chmod
less
cat
head
tail
wc
which
whatis
man
apropos
type
alias
ln
ln -s
stat
du -h
df -h
free -h
groups
file
uname -a
```

---

# Most Important Concepts

1. Linux file hierarchy starts at `/`
2. `.` = current directory
3. `..` = parent directory
4. `~` = home directory
5. Permissions (`rwx`)
6. Ownership (user/group)
7. `chmod`
8. Files vs directories
9. Hard links vs symbolic links
10. Options vs arguments
11. Recursive operations (`-r`)
12. Aliases
13. Using `man`, `whatis`, `apropos`
14. Virtual filesystems (`/proc`, `/sys`)
15. Basic file manipulation (`touch`, `cp`, `mv`, `rm`) 

#review 