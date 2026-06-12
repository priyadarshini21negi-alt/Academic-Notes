# ── NAVIGATION ──────────────────────────────────────────

What command lists files in the current directory? ;; ls

What command lists files with detailed info (permissions, owner, size, date)? ;; ls -l

What command shows inode numbers alongside filenames? ;; ls -i

What command shows the directory entry itself rather than its contents? ;; ls -d _**directory**_

What is the long form of the ls -i option? ;; --inode

What is the long form of the ls -d option? ;; --directory

Does the order of options matter for the ls command? ;; No — ls accepts options in any order

What command changes to a directory? ;; cd _**directory**_

What command returns to the home directory? ;; cd

What command returns to the home directory using a shortcut? ;; cd ~

What command goes to the previous working directory? ;; cd -

What command goes up one level? ;; cd ..

What does . represent in Linux? ;; The current directory

What does .. represent in Linux? ;; The parent directory

What does ~ represent in Linux? ;; The home directory

What does - represent when used with cd? ;; The previous working directory

What is the root directory in Linux? ;; /

What is the parent directory of the root? ;; The root directory itself

# ── DATE AND TIME ───────────────────────────────────────

What command displays the current date and time? ;; date

What option makes date output in RFC 5322 format? ;; date -R

# ── CALENDAR ────────────────────────────────────────────

What command displays the current month's calendar? ;; cal

What command displays a specific month and year calendar? ;; cal _**month**_ _**year**_

What command displays a calendar vertically? ;; ncal

# ── MEMORY AND GROUPS ───────────────────────────────────

What command displays memory statistics? ;; free

What command displays memory statistics in human-readable format? ;; free -h

What command lists the groups a user belongs to? ;; groups

What is swap memory? ;; Disk space used as overflow when RAM is full

Why is swap slower than RAM? ;; Disk access is much slower than physical memory

# ── FILE AND DIRECTORY OPERATIONS ───────────────────────

What command creates a directory? ;; mkdir _**directory**_

What command creates an empty file? ;; touch _**file**_

What command copies a file? ;; cp _**source**_ _**destination**_

What command recursively copies a directory? ;; cp -r _**source**_ _**destination**_

What command moves a file? ;; mv _**source**_ _**destination**_

What command renames a file? ;; mv _**oldname**_ _**newname**_

What command removes a file? ;; rm _**file**_

What command removes an empty directory? ;; rmdir _**directory**_
<!--SR:!2026-06-14,2,246-->

What command removes a directory recursively? ;; rm -r _**directory**_

What command removes a file with a confirmation prompt? ;; rm -i _**file**_

Why does mv not need a -r flag to move a directory, but cp does? ;; mv just moves the directory entry; cp must copy all contents recursively

What command creates multiple empty files at once? ;; touch _**file1**_ _**file2**_ _**file3**_

# ── VIEWING FILE CONTENTS ───────────────────────────────

What command displays the entire contents of a file? ;; cat _**file**_

What command displays a file page-by-page? ;; less _**file**_

What command also displays a file page-by-page? ;; more _**file**_

What is the practical difference between more and less? ;; less supports backward navigation and is more feature-rich

What command displays the first 10 lines of a file? ;; head _**file**_

What command displays the first N lines of a file? ;; head -n _**N**_ _**file**_

What command displays the last 10 lines of a file? ;; tail _**file**_

What command displays the last N lines of a file? ;; tail -n _**N**_ _**file**_

What command counts lines, words and bytes in a file? ;; wc _**file**_

What command counts only lines in a file? ;; wc -l _**file**_

# ── HELP AND DOCUMENTATION ──────────────────────────────

What command locates the executable path of a command? ;; which _**command**_

What command gives a one-line description of a command? ;; whatis _**command**_

What command opens the manual page of a command? ;; man _**command**_

What command searches for commands by keyword? ;; apropos _**keyword**_

What command is equivalent to apropos? ;; man -k _**keyword**_

What command lists Bash builtins and keywords? ;; help

What command opens an interactive documentation browser? ;; info

What command tells whether something is an alias, builtin or executable? ;; type _**command**_

# ── ALIASES ─────────────────────────────────────────────

What is an alias? ;; A user-defined shortcut for a command

What command creates an alias? ;; alias _**name**_=_**'command'**_

What command lists all currently defined aliases? ;; alias

What command removes an alias? ;; unalias _**name**_

Why do many users alias rm to rm -i? ;; To avoid accidental deletion

# ── FILE INFORMATION ────────────────────────────────────

What command displays the type of a file? ;; file _**file**_

What command displays detailed file metadata? ;; stat _**file**_

What command shows disk usage of a file or directory? ;; du _**file**_

What command shows disk usage in human-readable form? ;; du -h _**file**_

What command shows overall filesystem disk space usage? ;; df -h

What information does wc provide? ;; Number of lines, words and bytes
<!--SR:!2026-06-13,1,230-->

What does stat provide? ;; Detailed file metadata including size, permissions and timestamps

What command prints the current logged-in username? ;; whoami
<!--SR:!2026-06-13,1,226-->

# ── FILE PERMISSIONS ────────────────────────────────────

What command changes file permissions? ;; chmod _**permissions**_ _**file**_

What command removes write permission from the group? ;; chmod g-w _**file**_

What command removes execute permission from the group? ;; chmod g-x _**file**_

What command removes execute permission from others? ;; chmod o-x _**file**_

What command adds read permission to others? ;; chmod o+r _**file**_

What are the three categories of Linux permissions? ;; Owner, Group, Others

What are the three basic Linux permissions? ;; Read, Write, Execute

What numerical value corresponds to read permission? ;; 4

What numerical value corresponds to write permission? ;; 2

What numerical value corresponds to execute permission? ;; 1

What permission does 7 represent? ;; rwx

What permission does 6 represent? ;; rw-

What permission does 5 represent? ;; r-x

What permission does 4 represent? ;; r--
<!--SR:!2026-06-13,1,226-->

What does permission 700 mean? ;; Full permissions for owner; none for group or others

What does permission 755 mean? ;; Full permissions for owner; read and execute for group and others

What does permission 644 mean? ;; Read and write for owner; read-only for group and others

# ── FILESYSTEM CONCEPTS ─────────────────────────────────

What is an inode? ;; A data structure storing a file's metadata

Does an inode store the filename? ;; No

What information does an inode store? ;; Permissions, ownership, timestamps and disk block locations

How can two filenames be identified as hard links to each other? ;; They share the same inode number

What is a hard link? ;; A directory entry pointing to the same inode as another entry

What is a symbolic link? ;; A file that stores the path to another file or directory

Do hard links share inode numbers? ;; Yes

Do symbolic links share inode numbers with the original file? ;; No

What happens if one hard link is deleted? ;; The file remains accessible through the remaining hard links

What happens if the target of a symbolic link is deleted? ;; The symbolic link becomes broken

What command creates a symbolic link? ;; ln -s _**source**_ _**link**_

What command creates a hard link? ;; ln _**source**_ _**link**_
<!--SR:!2026-06-13,1,226-->

# ── LS -L OUTPUT FORMAT ─────────────────────────────────

What does the first character in ls -l output indicate? ;; The file type

What does - at the start of ls -l output indicate? ;; A regular file

What does d at the start of ls -l output indicate? ;; A directory

What does l at the start of ls -l output indicate? ;; A symbolic link

What does c at the start of ls -l output indicate? ;; A character device

What does b at the start of ls -l output indicate? ;; A block device

What does s at the start of ls -l output indicate? ;; A socket

What does p at the start of ls -l output indicate? ;; A named pipe

What is the hard link count shown in ls -l? ;; The number of directory entries pointing to the same inode

Why does every directory contain a . entry? ;; It is a hard link to itself

Why does every directory contain a .. entry? ;; It is a hard link to its parent directory

# ── VIRTUAL FILESYSTEMS ─────────────────────────────────

What is the /proc filesystem? ;; A virtual filesystem exposing kernel and process information

Are files in /proc stored on disk? ;; No

Why do some files in /proc show size 0 but still contain data? ;; They are generated dynamically by the kernel

What do the numbered directories inside /proc represent? ;; Process IDs (PIDs)

What is the /sys filesystem? ;; A virtual filesystem exposing hardware and device information

Why are /proc and /sys called virtual filesystems? ;; They expose runtime kernel information rather than storing files on disk

What information can be found in /proc/cpuinfo? ;; CPU details

What information can be found in /proc/meminfo? ;; Memory details

What information can be found in /proc/version? ;; Kernel version details

What information can be found in /proc/partitions? ;; Disk partition information

What command shows kernel name, version and system architecture? ;; uname -a

# ── GENERAL CONCEPTS ────────────────────────────────────

What is a shell builtin? ;; A command implemented directly inside the shell
<!--SR:!2026-06-13,1,230-->

What is an executable command? ;; A command provided by a binary file

What is the difference between an option and an argument? ;; Options modify behaviour; arguments specify targets

What is recursion in file operations? ;; Performing an operation on a directory and all its contents

Why is recursive deletion dangerous? ;; It can delete entire directory trees

What causes a Permission Denied error? ;; Lack of required permissions
<!--SR:!2026-06-13,1,226-->

Why is Linux considered relatively safe for beginners? ;; Permissions prevent accidental modification of most system files