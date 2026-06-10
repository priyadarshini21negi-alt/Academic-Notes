# ── NAVIGATION ──────────────────────────────────────────

What command prints the current working directory? ;; pwd

What command lists files in the current directory? ;; ls

What command lists files with detailed info (permissions, owner, size, date)? ;; ls -l

What command lists all files including hidden ones? ;; ls -a

What command lists files with sizes in human-readable form? ;; ls -lh

What command lists files sorted by modification time, newest first? ;; ls -lt

What command shows inode numbers alongside filenames? ;; ls -i

What command shows the directory entry itself rather than its contents? ;; ls -d _**directory**_

What command recursively lists all files in a directory tree? ;; ls -R _**directory**_

What is the long form of the ls -i option? ;; --inode

What is the long form of the ls -d option? ;; --directory

What prefix is used for long-form options in Linux commands? ;; -- (double dash), e.g. --inode instead of -i

Does the order of options matter for the ls command? ;; No — ls accepts options in any order

What command changes to a directory? ;; cd _**directory**_

What command returns to the home directory? ;; cd ~

What command goes to the previous working directory? ;; cd -

What command goes up one level? ;; cd ..

# ── DATE AND TIME ───────────────────────────────────────

What command displays the current date and time? ;; date

What option makes date output in RFC 5322 format (used in email)? ;; date -R

What syntax formats date output with custom fields? ;; date +_**format**_ (e.g. date +"%Y-%m-%d")

# ── CALENDAR ────────────────────────────────────────────

What command displays the current month's calendar? ;; cal

<!--SR:!2026-06-13,4,270-->

What command displays a specific month and year calendar? ;; cal _**month**_ _**year**_

<!--SR:!2026-06-13,4,270-->

# ── FILE AND DIRECTORY OPERATIONS ───────────────────────

What command creates a directory? ;; mkdir _**directory**_

<!--SR:!2026-06-12,3,265-->

What command creates nested directories in one go? ;; mkdir -p _**path/to/dir**_

What command creates an empty file? ;; touch _**file**_

<!--SR:!2026-06-13,4,270-->

What command copies a file? ;; cp _**source**_ _**destination**_

<!--SR:!2026-06-10,1,230-->

What command copies a file with a confirmation prompt before overwriting? ;; cp -i _**source**_ _**destination**_

What command recursively copies a directory? ;; cp -r _**source**_ _**destination**_

<!--SR:!2026-06-12,3,250-->

What command moves a file? ;; mv _**source**_ _**destination**_

<!--SR:!2026-06-12,3,250-->

What command renames a file? ;; mv _**oldname**_ _**newname**_

<!--SR:!2026-06-10,1,230-->

Why does mv not need a -r flag to move a directory, but cp does? ;; mv just renames a directory entry in place — no data is copied; cp must duplicate all contents recursively

What command creates multiple empty files at once? ;; touch _**file1**_ _**file2**_ _**file3**_

What command removes a file? ;; rm _**file**_

<!--SR:!2026-06-13,4,270-->

What command removes a directory recursively? ;; rm -r _**directory**_

<!--SR:!2026-06-12,3,265-->

What command removes a file with a confirmation prompt? ;; rm -i _**file**_

What command creates a symbolic link? ;; ln -s _**source**_ _**link**_

<!--SR:!2026-06-10,1,225-->

What command creates a hard link? ;; ln _**source**_ _**link**_

<!--SR:!2026-06-10,1,225-->

# ── VIEWING FILE CONTENTS ───────────────────────────────

What command displays the entire contents of a file? ;; cat _**file**_

<!--SR:!2026-06-10,1,230-->

What command displays a file page-by-page? ;; less _**file**_

<!--SR:!2026-06-10,1,230-->

What command also displays a file page-by-page, similar to less? ;; more _**file**_

What is the practical difference between more and less? ;; less supports backward navigation and is more feature-rich; more only goes forward. Less is also a larger binary — the Linux joke is "less is more"

What is the difference between less and cat? ;; less allows page-by-page navigation; cat prints everything at once

When is less preferred over cat? ;; For large files

What command displays the first 10 lines of a file? ;; head _**file**_

<!--SR:!2026-06-12,3,265-->

What command displays the first N lines of a file? ;; head -n _**N**_ _**file**_

<!--SR:!2026-06-12,3,265-->

What command displays the last 10 lines of a file? ;; tail _**file**_

<!--SR:!2026-06-13,4,270-->

What command displays the last N lines of a file? ;; tail -n _**N**_ _**file**_

<!--SR:!2026-06-12,3,265-->

What command follows a file in real-time as it grows? ;; tail -f _**file**_

What command counts lines, words and bytes in a file? ;; wc _**file**_

<!--SR:!2026-06-10,1,225-->

What command counts only lines in a file? ;; wc -l _**file**_

<!--SR:!2026-06-10,1,230-->

# ── SEARCHING ───────────────────────────────────────────

What command searches for a pattern inside a file? ;; grep _**pattern**_ _**file**_

What command searches recursively through a directory? ;; grep -r _**pattern**_ _**directory**_

What command searches ignoring case? ;; grep -i _**pattern**_ _**file**_

What command shows line numbers alongside grep matches? ;; grep -n _**pattern**_ _**file**_

What command shows only filenames that contain a match? ;; grep -l _**pattern**_ _**files**_

What command inverts a grep search (shows non-matching lines)? ;; grep -v _**pattern**_ _**file**_

What command finds files by name? ;; find _**directory**_ -name _**filename**_

What command finds only regular files? ;; find _**directory**_ -type f

What command finds only directories? ;; find _**directory**_ -type d

What command finds files modified in the last N days? ;; find _**directory**_ -mtime -_**N**_

What command finds files larger than a given size? ;; find _**directory**_ -size +_**N**_k

# ── TEXT PROCESSING ─────────────────────────────────────

What command prints a line of text to the terminal? ;; echo _**text**_

What command prints the value of a variable? ;; echo $_**VARIABLE**_

What command sorts lines of a file alphabetically? ;; sort _**file**_

What command sorts lines in reverse order? ;; sort -r _**file**_

What command sorts lines numerically? ;; sort -n _**file**_

What command removes consecutive duplicate lines? ;; uniq _**file**_

What command counts occurrences of each unique line? ;; uniq -c _**file**_

What command extracts specific columns from a file? ;; cut -d _**delimiter**_ -f _**field**_ _**file**_

What command shows the differences between two files? ;; diff _**file1**_ _**file2**_

What command translates or deletes characters in a stream? ;; tr _**set1**_ _**set2**_

# ── PIPES AND REDIRECTION ───────────────────────────────

What does the pipe operator | do? ;; Passes the output of one command as input to the next

What does > do? ;; Redirects stdout to a file, overwriting it

What does >> do? ;; Redirects stdout to a file, appending to it

What does < do? ;; Redirects a file as stdin to a command

What does 2> do? ;; Redirects stderr to a file

What does 2>&1 do? ;; Redirects stderr into the same stream as stdout

What does > /dev/null do? ;; Discards output by sending it to the null device

What is stdin? ;; Standard input — file descriptor 0

What is stdout? ;; Standard output — file descriptor 1

What is stderr? ;; Standard error — file descriptor 2

# ── FILE PERMISSIONS ────────────────────────────────────

What command changes file permissions? ;; chmod _**permissions**_ _**file**_

<!--SR:!2026-06-10,1,230-->

What command removes write permission from the group? ;; chmod g-w _**file**_

<!--SR:!2026-06-10,1,230-->

What command removes execute permission from the group? ;; chmod g-x _**file**_

<!--SR:!2026-06-10,1,230-->

What command adds read permission to others? ;; chmod o+r _**file**_

<!--SR:!2026-06-10,1,230-->

What command changes the owner of a file? ;; chown _**user**_ _**file**_

What command changes both owner and group of a file? ;; chown _**user**_:_**group**_ _**file**_

What command changes only the group of a file? ;; chgrp _**group**_ _**file**_

What are the three categories of Linux permissions? ;; Owner, Group, Others

What are the three basic Linux permissions? ;; Read, Write, Execute

<!--SR:!2026-06-10,1,225-->

What does read permission allow on a file? ;; Viewing the contents of the file

What does write permission allow on a file? ;; Modifying the file

What does execute permission allow on a file? ;; Running the file as a program

<!--SR:!2026-06-10,1,225-->

What does read permission allow on a directory? ;; Listing the directory's contents

What does write permission allow on a directory? ;; Creating or removing files inside the directory

What does execute permission allow on a directory? ;; Entering or traversing the directory

What numerical value corresponds to read permission? ;; 4

What numerical value corresponds to write permission? ;; 2

What numerical value corresponds to execute permission? ;; 1

What permission does 7 represent? ;; rwx (read + write + execute)

What permission does 6 represent? ;; rw- (read + write)

What permission does 5 represent? ;; r-x (read + execute)

<!--SR:!2026-06-10,1,225-->

What permission does 4 represent? ;; r-- (read only)

What does permission 700 mean? ;; Full permissions for owner; none for group or others

What does permission 755 mean? ;; Full permissions for owner; read and execute for group and others

What does permission 644 mean? ;; Read and write for owner; read-only for group and others

# ── USER AND SESSION ─────────────────────────────────────

What command prints the current logged-in username? ;; whoami

What command shows the current user's UID, GID and groups? ;; id

What command lists the groups a user belongs to? ;; groups

What command runs a command with superuser privileges? ;; sudo _**command**_

What command switches to another user account? ;; su - _**username**_

What command changes a user's password? ;; passwd

# ── HELP AND DOCUMENTATION ──────────────────────────────

What command locates the executable path of a command? ;; which _**command**_

<!--SR:!2026-06-10,1,230-->

What command gives a one-line description of a command? ;; whatis _**command**_

<!--SR:!2026-06-12,3,250-->

What command opens the manual page of a command? ;; man _**command**_

<!--SR:!2026-06-13,4,270-->

What command searches for commands by keyword? ;; apropos _**keyword**_

<!--SR:!2026-06-10,1,225-->

What command is equivalent to apropos? ;; man -k _**keyword**_

<!--SR:!2026-06-10,1,230-->

What command tells whether something is an alias, builtin or executable? ;; type _**command**_

<!--SR:!2026-06-12,3,250-->

# ── FILE INFORMATION ────────────────────────────────────

What command displays the type of a file? ;; file _**file**_

<!--SR:!2026-06-10,1,225-->

What command displays detailed file metadata? ;; stat _**file**_

<!--SR:!2026-06-10,1,230-->

What command shows disk usage of a file or directory? ;; du _**file**_

<!--SR:!2026-06-10,1,230-->

What command shows disk usage in human-readable form? ;; du -h _**file**_

<!--SR:!2026-06-10,1,225-->

What command shows overall filesystem disk space usage? ;; df -h

What information does wc provide? ;; Number of lines, words and bytes

What does stat provide? ;; Detailed file metadata including size, permissions and timestamps

What are the three file timestamps in Linux? ;; atime (last access), mtime (last modification), ctime (last status change)

What does the touch command do to an existing file? ;; Updates its timestamps

What does the touch command do to a nonexistent file? ;; Creates an empty file

# ── PROCESS MANAGEMENT ──────────────────────────────────

What command lists processes running in the current terminal? ;; ps

What command lists all running processes with full detail? ;; ps aux

What command shows a live view of running processes? ;; top

What command sends a termination signal to a process by PID? ;; kill _**PID**_

What command forcefully kills a process? ;; kill -9 _**PID**_

What command kills all processes with a given name? ;; killall _**name**_

What does & at the end of a command do? ;; Runs the command in the background

What command lists background and stopped jobs? ;; jobs

What command brings a background job to the foreground? ;; fg _**%jobnumber**_

What command resumes a stopped job in the background? ;; bg _**%jobnumber**_

What key combination sends an interrupt signal to the foreground process? ;; Ctrl + C

What key combination suspends the foreground process? ;; Ctrl + Z

# ── SYSTEM INFORMATION ──────────────────────────────────

What command shows kernel name, version and system architecture? ;; uname -a

What command shows the system hostname? ;; hostname

What command displays the current date and time? ;; date

What command shows how long the system has been running? ;; uptime

What command displays human-readable memory statistics? ;; free -h

<!--SR:!2026-06-10,1,225-->

What command displays human-readable disk space usage per filesystem? ;; df -h

What information can be found in /proc/cpuinfo? ;; CPU details

What information can be found in /proc/meminfo? ;; Memory details

What information can be found in /proc/version? ;; Kernel version details

What information can be found in /proc/partitions? ;; Disk partition information

<!--SR:!2026-06-10,1,225-->

# ── SHELL HISTORY AND SHORTCUTS ─────────────────────────

What command displays the command history? ;; history

What repeats the last command? ;; !!

What runs command number N from history? ;; !_**N**_

What key combination searches command history interactively? ;; Ctrl + R

What key clears the terminal screen? ;; Ctrl + L

# ── WILDCARDS AND GLOBBING ──────────────────────────────

What does the wildcard * match? ;; Zero or more of any characters

What does the wildcard ? match? ;; Exactly one character

What does [abc] match in a glob pattern? ;; Any single character listed (a, b, or c)

What does [a-z] match in a glob pattern? ;; Any single character in the given range

What does [!abc] match in a glob pattern? ;; Any single character NOT in the list

# ── ARCHIVES AND COMPRESSION ────────────────────────────

What command creates a compressed tar archive? ;; tar -czf _**archive.tar.gz**_ _**files**_

What command extracts a compressed tar archive? ;; tar -xzf _**archive.tar.gz**_

What command lists the contents of a tar archive without extracting? ;; tar -tzf _**archive.tar.gz**_

What command compresses a file with gzip? ;; gzip _**file**_

What command decompresses a gzip file? ;; gunzip _**file.gz**_

What command creates a zip archive? ;; zip _**archive.zip**_ _**files**_

What command extracts a zip archive? ;; unzip _**archive.zip**_

# ── ENVIRONMENT AND VARIABLES ───────────────────────────

What command lists all environment variables? ;; env

What command sets and exports a variable for child processes? ;; export _**VAR**_=_**value**_

What does the PATH variable contain? ;; A colon-separated list of directories where the shell looks for commands

What does the HOME variable contain? ;; The path to the current user's home directory

What does the USER variable contain? ;; The name of the current logged-in user

# ── FILESYSTEM CONCEPTS ─────────────────────────────────

What is the root directory in Linux? ;; /

<!--SR:!2026-06-10,1,225-->

What does the root directory represent? ;; The topmost directory from which the entire filesystem hierarchy starts

What does . represent in Linux? ;; The current directory

What does .. represent in Linux? ;; The parent directory

What does ~ represent in Linux? ;; The home directory

<!--SR:!2026-06-12,3,265-->

What does - represent when used with cd? ;; The previous working directory

What is the parent directory of the root? ;; The root directory itself (it points to itself)

What is an inode? ;; A data structure storing a file's metadata — permissions, ownership, timestamps and disk location

Does an inode store the filename? ;; No — filenames are stored in the directory entry, not the inode

What information does an inode store? ;; Permissions, ownership, timestamps and disk block locations

How can two filenames be identified as hard links to each other? ;; They share the same inode number

What is a hard link? ;; A directory entry that points to the same inode as another entry

What is a symbolic link? ;; A separate file that stores the path to another file or directory

Do hard links share inode numbers? ;; Yes

Do symbolic links share inode numbers with the original file? ;; No

What happens if one hard link to a file is deleted? ;; The file remains accessible through the remaining hard links

What happens if the target of a symbolic link is deleted? ;; The symlink becomes broken (dangling)

What is a filesystem block? ;; The smallest allocation unit on disk

Why does even a tiny file consume a full block? ;; Files are allocated in whole blocks; no two files share a block

Why can disk usage be larger than actual file size? ;; Files always occupy at least one full block regardless of how little data they contain

# ── LS -L OUTPUT FORMAT ─────────────────────────────────

What does the first character in ls -l output indicate? ;; The file type

What does - at the start of ls -l output indicate? ;; A regular file

<!--SR:!2026-06-10,1,225-->

What does d at the start of ls -l output indicate? ;; A directory

<!--SR:!2026-06-12,3,265-->

What does l at the start of ls -l output indicate? ;; A symbolic link

What does c at the start of ls -l output indicate? ;; A character device (transfers data char by char, e.g. a terminal)

What does b at the start of ls -l output indicate? ;; A block device (transfers data in blocks, e.g. a hard disk)

What does s at the start of ls -l output indicate? ;; A socket (used for two-way inter-process communication)

What does p at the start of ls -l output indicate? ;; A named pipe (used for one-way inter-process communication)

<!--SR:!2026-06-10,1,225-->

What is the hard link count shown in ls -l? ;; The number of directory entries pointing to the same inode

Why does every directory contain a . entry? ;; It is a hard link to the directory itself

<!--SR:!2026-06-10,1,225-->

Why does every directory contain a .. entry? ;; It is a hard link to the parent directory

# ── VIRTUAL FILESYSTEMS ─────────────────────────────────

What is the /proc filesystem? ;; A virtual filesystem that exposes kernel and process information

Are files in /proc stored on disk? ;; No — they are generated dynamically by the kernel

<!--SR:!2026-06-10,1,225-->

Why do some files in /proc show size 0 but still contain data? ;; They are generated on-the-fly; the size is not pre-calculated

What do the numbered directories inside /proc represent? ;; Each number is a process ID (PID); those directories hold information about that running process

What is the /sys filesystem? ;; A virtual filesystem exposing hardware, device and driver information

Why is /sys considered better organised than /proc for hardware info? ;; /sys was designed later with a cleaner directory structure specifically for device and driver data

Why are /proc and /sys called virtual filesystems? ;; They present runtime kernel data as files, storing nothing on disk

What is the relationship between the apropos and whatis executables? ;; They are actually the same binary — it detects which name it was invoked under and changes its behaviour accordingly

# ── MEMORY AND STORAGE ──────────────────────────────────

What is RAM? ;; Fast primary memory used by running programs

<!--SR:!2026-06-11,2,245-->

What is swap memory? ;; Disk space used as overflow when RAM is full

Why is swap slower than RAM? ;; Disk access is orders of magnitude slower than physical memory

# ── GENERAL CONCEPTS ─────────────────────────────────────

What is a shell builtin? ;; A command implemented directly inside the shell itself

What is an executable command? ;; A command provided by a binary file stored on the filesystem

What is an alias? ;; A user-defined shortcut for a command or series of commands

What command creates an alias? ;; alias _**name**_=_**'command'**_

What command lists all currently defined aliases? ;; alias

What command removes an alias? ;; unalias _**name**_

What command lists all bash shell keywords and builtins? ;; help

What command opens an interactive documentation browser for Linux commands? ;; info

What command opens info at a specific command's page? ;; info _**command**_

Why do many users alias rm to rm -i? ;; To get a confirmation prompt and avoid accidental deletion

What is the difference between an option and an argument? ;; Options modify how a command behaves; arguments specify what it operates on

What is recursion in file operations? ;; Performing an operation on a directory and all its contents recursively

Why is recursive deletion dangerous? ;; It silently deletes entire directory trees with no undo

What is the root user? ;; The superuser account with unrestricted access to the entire system

Why can ordinary users not modify most system files? ;; Those files are owned by root and protected by restrictive permissions

What causes a Permission Denied error? ;; The process lacks the required permission for the attempted operation

Why is Linux considered relatively safe for beginners exploring commands? ;; Permissions prevent most commands from accidentally damaging system files