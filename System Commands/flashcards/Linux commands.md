# ── NAVIGATION ──────────────────────────────────────────

What command lists files in the current directory? ;; ls
<!--SR:!2026-06-14,2,246-->

What command lists files with detailed info (permissions, owner, size, date)? ;; ls -l
<!--SR:!2026-06-14,2,246-->

What command shows inode numbers alongside filenames? ;; ls -i
<!--SR:!2026-06-14,2,246-->

What command shows the directory entry itself rather than its contents? ;; ls -d _**directory**_
<!--SR:!2026-06-13,1,226-->

What is the long form of the ls -i option? ;; --inode
<!--SR:!2026-06-13,1,226-->

What is the long form of the ls -d option? ;; --directory
<!--SR:!2026-06-15,3,266-->

Does the order of options matter for the ls command? ;; No — ls accepts options in any order
<!--SR:!2026-06-14,2,246-->

What command changes to a directory? ;; cd _**directory**_
<!--SR:!2026-06-15,3,266-->

What command returns to the home directory? ;; cd
<!--SR:!2026-06-15,3,266-->

What command returns to the home directory using a shortcut? ;; cd ~
<!--SR:!2026-06-15,3,266-->

What command goes to the previous working directory? ;; cd -
<!--SR:!2026-06-15,3,266-->

What command goes up one level? ;; cd ..
<!--SR:!2026-06-15,3,266-->

What does . represent in Linux? ;; The current directory
<!--SR:!2026-06-15,3,266-->

What does .. represent in Linux? ;; The parent directory
<!--SR:!2026-06-15,3,266-->

What does ~ represent in Linux? ;; The home directory
<!--SR:!2026-06-15,3,266-->

What does - represent when used with cd? ;; The previous working directory
<!--SR:!2026-06-14,2,246-->

What is the root directory in Linux? ;; /
<!--SR:!2026-06-15,3,266-->

What is the parent directory of the root? ;; The root directory itself
<!--SR:!2026-06-15,3,266-->

# ── DATE AND TIME ───────────────────────────────────────

What command displays the current date and time? ;; date
<!--SR:!2026-06-15,3,266-->

What option makes date output in RFC 5322 format? ;; date -R
<!--SR:!2026-06-15,3,266-->

# ── CALENDAR ────────────────────────────────────────────

What command displays the current month's calendar? ;; cal
<!--SR:!2026-06-15,3,266-->

What command displays a specific month and year calendar? ;; cal _**month**_ _**year**_
<!--SR:!2026-06-15,3,266-->

What command displays a calendar vertically? ;; ncal
<!--SR:!2026-06-15,3,266-->

# ── MEMORY AND GROUPS ───────────────────────────────────

What command displays memory statistics? ;; free
<!--SR:!2026-06-13,1,226-->

What command displays memory statistics in human-readable format? ;; free -h
<!--SR:!2026-06-14,2,246-->

What command lists the groups a user belongs to? ;; groups
<!--SR:!2026-06-15,3,266-->

What is swap memory? ;; Disk space used as overflow when RAM is full
<!--SR:!2026-06-15,3,266-->

Why is swap slower than RAM? ;; Disk access is much slower than physical memory
<!--SR:!2026-06-13,1,226-->

# ── FILE AND DIRECTORY OPERATIONS ───────────────────────

What command creates a directory? ;; mkdir _**directory**_
<!--SR:!2026-06-15,3,266-->

What command creates an empty file? ;; touch _**file**_
<!--SR:!2026-06-15,3,266-->

What command copies a file? ;; cp _**source**_ _**destination**_
<!--SR:!2026-06-15,3,266-->

What command recursively copies a directory? ;; cp -r _**source**_ _**destination**_
<!--SR:!2026-06-14,2,246-->

What command moves a file? ;; mv _**source**_ _**destination**_
<!--SR:!2026-06-15,3,266-->

What command renames a file? ;; mv _**oldname**_ _**newname**_
<!--SR:!2026-06-13,1,226-->

What command removes a file? ;; rm _**file**_
<!--SR:!2026-06-15,3,266-->

What command removes an empty directory? ;; rmdir _**directory**_
<!--SR:!2026-06-14,2,246-->

What command removes a directory recursively? ;; rm -r _**directory**_
<!--SR:!2026-06-15,3,266-->

What command removes a file with a confirmation prompt? ;; rm -i _**file**_
<!--SR:!2026-06-15,3,266-->

Why does mv not need a -r flag to move a directory, but cp does? ;; mv just moves the directory entry; cp must copy all contents recursively
<!--SR:!2026-06-13,1,226-->

What command creates multiple empty files at once? ;; touch _**file1**_ _**file2**_ _**file3**_
<!--SR:!2026-06-14,2,246-->

# ── VIEWING FILE CONTENTS ───────────────────────────────

What command displays the entire contents of a file? ;; cat _**file**_
<!--SR:!2026-06-13,1,226-->

What command displays a file page-by-page? ;; less _**file**_
<!--SR:!2026-06-13,1,226-->

What command also displays a file page-by-page? ;; more _**file**_
<!--SR:!2026-06-13,1,226-->

What is the practical difference between more and less? ;; less supports backward navigation and is more feature-rich
<!--SR:!2026-06-13,1,226-->

What command displays the first 10 lines of a file? ;; head _**file**_
<!--SR:!2026-06-15,3,266-->

What command displays the first N lines of a file? ;; head -n _**N**_ _**file**_
<!--SR:!2026-06-15,3,266-->

What command displays the last 10 lines of a file? ;; tail _**file**_
<!--SR:!2026-06-15,3,266-->

What command displays the last N lines of a file? ;; tail -n _**N**_ _**file**_
<!--SR:!2026-06-15,3,266-->

What command counts lines, words and bytes in a file? ;; wc _**file**_
<!--SR:!2026-06-13,1,226-->

What command counts only lines in a file? ;; wc -l _**file**_
<!--SR:!2026-06-13,1,226-->

# ── HELP AND DOCUMENTATION ──────────────────────────────

What command locates the executable path of a command? ;; which _**command**_
<!--SR:!2026-06-13,1,226-->

What command gives a one-line description of a command? ;; whatis _**command**_
<!--SR:!2026-06-15,3,266-->

What command opens the manual page of a command? ;; man _**command**_
<!--SR:!2026-06-13,1,226-->

What command searches for commands by keyword? ;; apropos _**keyword**_
<!--SR:!2026-06-13,1,226-->

What command is equivalent to apropos? ;; man -k _**keyword**_
<!--SR:!2026-06-13,1,226-->

What command lists Bash builtins and keywords? ;; help
<!--SR:!2026-06-14,2,246-->

What command opens an interactive documentation browser? ;; info
<!--SR:!2026-06-13,1,226-->

What command tells whether something is an alias, builtin or executable? ;; type _**command**_
<!--SR:!2026-06-13,1,226-->

# ── ALIASES ─────────────────────────────────────────────

What is an alias? ;; A user-defined shortcut for a command
<!--SR:!2026-06-14,2,246-->

What command creates an alias? ;; alias _**name**_=_**'command'**_
<!--SR:!2026-06-14,2,246-->

What command lists all currently defined aliases? ;; alias
<!--SR:!2026-06-14,2,246-->

What command removes an alias? ;; unalias _**name**_
<!--SR:!2026-06-13,1,226-->

Why do many users alias rm to rm -i? ;; To avoid accidental deletion
<!--SR:!2026-06-13,1,226-->

# ── FILE INFORMATION ────────────────────────────────────

What command displays the type of a file? ;; file _**file**_
<!--SR:!2026-06-13,1,226-->

What command displays detailed file metadata? ;; stat _**file**_
<!--SR:!2026-06-13,1,226-->

What command shows disk usage of a file or directory? ;; du _**file**_
<!--SR:!2026-06-15,3,266-->

What command shows disk usage in human-readable form? ;; du -h _**file**_
<!--SR:!2026-06-14,2,246-->

What command shows overall filesystem disk space usage? ;; df -h
<!--SR:!2026-06-13,1,226-->

What information does wc provide? ;; Number of lines, words and bytes
<!--SR:!2026-06-13,1,230-->

What does stat provide? ;; Detailed file metadata including size, permissions and timestamps
<!--SR:!2026-06-14,2,246-->

What command prints the current logged-in username? ;; whoami
<!--SR:!2026-06-13,1,226-->

# ── FILE PERMISSIONS ────────────────────────────────────

What command changes file permissions? ;; chmod _**permissions**_ _**file**_
<!--SR:!2026-06-14,2,246-->

What command removes write permission from the group? ;; chmod g-w _**file**_
<!--SR:!2026-06-13,1,226-->

What command removes execute permission from the group? ;; chmod g-x _**file**_
<!--SR:!2026-06-13,1,226-->

What command removes execute permission from others? ;; chmod o-x _**file**_
<!--SR:!2026-06-13,1,226-->

What command adds read permission to others? ;; chmod o+r _**file**_
<!--SR:!2026-06-14,2,246-->

What are the three categories of Linux permissions? ;; Owner, Group, Others
<!--SR:!2026-06-13,1,226-->

What are the three basic Linux permissions? ;; Read, Write, Execute
<!--SR:!2026-06-15,3,266-->

What numerical value corresponds to read permission? ;; 4
<!--SR:!2026-06-13,1,226-->

What numerical value corresponds to write permission? ;; 2
<!--SR:!2026-06-13,1,226-->

What numerical value corresponds to execute permission? ;; 1
<!--SR:!2026-06-13,1,226-->

What permission does 7 represent? ;; rwx
<!--SR:!2026-06-13,1,226-->

What permission does 6 represent? ;; rw-
<!--SR:!2026-06-13,1,226-->

What permission does 5 represent? ;; r-x
<!--SR:!2026-06-13,1,226-->

What permission does 4 represent? ;; r--
<!--SR:!2026-06-13,1,226-->

What does permission 700 mean? ;; Full permissions for owner; none for group or others
<!--SR:!2026-06-13,1,226-->

What does permission 755 mean? ;; Full permissions for owner; read and execute for group and others
<!--SR:!2026-06-13,1,226-->

What does permission 644 mean? ;; Read and write for owner; read-only for group and others
<!--SR:!2026-06-13,1,226-->

# ── FILESYSTEM CONCEPTS ─────────────────────────────────

What is an inode? ;; A data structure storing a file's metadata
<!--SR:!2026-06-14,2,246-->

Does an inode store the filename? ;; No
<!--SR:!2026-06-15,3,266-->

What information does an inode store? ;; Permissions, ownership, timestamps and disk block locations
<!--SR:!2026-06-14,2,246-->

How can two filenames be identified as hard links to each other? ;; They share the same inode number
<!--SR:!2026-06-13,1,226-->

What is a hard link? ;; A directory entry pointing to the same inode as another entry
<!--SR:!2026-06-14,2,246-->

What is a symbolic link? ;; A file that stores the path to another file or directory
<!--SR:!2026-06-13,1,226-->

Do hard links share inode numbers? ;; Yes
<!--SR:!2026-06-13,1,226-->

Do symbolic links share inode numbers with the original file? ;; No
<!--SR:!2026-06-13,1,226-->

What happens if one hard link is deleted? ;; The file remains accessible through the remaining hard links
<!--SR:!2026-06-14,2,246-->

What happens if the target of a symbolic link is deleted? ;; The symbolic link becomes broken
<!--SR:!2026-06-14,2,246-->

What command creates a symbolic link? ;; ln -s _**source**_ _**link**_
<!--SR:!2026-06-13,1,226-->

What command creates a hard link? ;; ln _**source**_ _**link**_
<!--SR:!2026-06-13,1,226-->

# ── LS -L OUTPUT FORMAT ─────────────────────────────────

What does the first character in ls -l output indicate? ;; The file type
<!--SR:!2026-06-13,1,226-->

What does - at the start of ls -l output indicate? ;; A regular file
<!--SR:!2026-06-13,1,226-->

What does d at the start of ls -l output indicate? ;; A directory
<!--SR:!2026-06-14,2,246-->

What does l at the start of ls -l output indicate? ;; A symbolic link
<!--SR:!2026-06-13,1,226-->

What does c at the start of ls -l output indicate? ;; A character device
<!--SR:!2026-06-13,1,226-->

What does b at the start of ls -l output indicate? ;; A block device
<!--SR:!2026-06-13,1,226-->

What does s at the start of ls -l output indicate? ;; A socket
<!--SR:!2026-06-13,1,226-->

What does p at the start of ls -l output indicate? ;; A named pipe
<!--SR:!2026-06-13,1,226-->

What is the hard link count shown in ls -l? ;; The number of directory entries pointing to the same inode
<!--SR:!2026-06-13,1,226-->

Why does every directory contain a . entry? ;; It is a hard link to itself
<!--SR:!2026-06-13,1,226-->

Why does every directory contain a .. entry? ;; It is a hard link to its parent directory
<!--SR:!2026-06-13,1,226-->

# ── VIRTUAL FILESYSTEMS ─────────────────────────────────

What is the /proc filesystem? ;; A virtual filesystem exposing kernel and process information
<!--SR:!2026-06-13,1,226-->

Are files in /proc stored on disk? ;; No
<!--SR:!2026-06-13,1,226-->

Why do some files in /proc show size 0 but still contain data? ;; They are generated dynamically by the kernel
<!--SR:!2026-06-13,1,226-->

What do the numbered directories inside /proc represent? ;; Process IDs (PIDs)
<!--SR:!2026-06-13,1,226-->

What is the /sys filesystem? ;; A virtual filesystem exposing hardware and device information
<!--SR:!2026-06-13,1,226-->

Why are /proc and /sys called virtual filesystems? ;; They expose runtime kernel information rather than storing files on disk
<!--SR:!2026-06-13,1,226-->

What information can be found in /proc/cpuinfo? ;; CPU details
<!--SR:!2026-06-14,2,246-->

What information can be found in /proc/meminfo? ;; Memory details
<!--SR:!2026-06-14,2,246-->

What information can be found in /proc/version? ;; Kernel version details
<!--SR:!2026-06-13,1,226-->

What information can be found in /proc/partitions? ;; Disk partition information
<!--SR:!2026-06-13,1,226-->

What command shows kernel name, version and system architecture? ;; uname -a
<!--SR:!2026-06-13,1,226-->

# ── GENERAL CONCEPTS ────────────────────────────────────

What is a shell builtin? ;; A command implemented directly inside the shell
<!--SR:!2026-06-13,1,230-->

What is an executable command? ;; A command provided by a binary file
<!--SR:!2026-06-13,1,226-->

What is the difference between an option and an argument? ;; Options modify behaviour; arguments specify targets
<!--SR:!2026-06-13,1,226-->

What is recursion in file operations? ;; Performing an operation on a directory and all its contents
<!--SR:!2026-06-13,1,226-->

Why is recursive deletion dangerous? ;; It can delete entire directory trees
<!--SR:!2026-06-13,1,226-->

What causes a Permission Denied error? ;; Lack of required permissions
<!--SR:!2026-06-13,1,226-->

Why is Linux considered relatively safe for beginners? ;; Permissions prevent accidental modification of most system files
<!--SR:!2026-06-13,1,226--> 


![[Pasted image 20260612162907.png]] ? C. That creates and runs virtual machines D. That allows running multiple operating systems concurrently, while sharing hardware resources 


