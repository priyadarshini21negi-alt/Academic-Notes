What command displays the current month's calendar? ;; cal
<!--SR:!2026-06-13,4,270-->

What command displays a specific month and year calendar? ;; cal ***month*** ***year***
<!--SR:!2026-06-13,4,270-->

What command creates a directory? ;; mkdir ***directory***
<!--SR:!2026-06-12,3,265-->

What command creates an empty file? ;; touch ***file***
<!--SR:!2026-06-13,4,270-->

What command copies a file? ;; cp ***source*** ***destination***
<!--SR:!2026-06-10,1,230-->

What command recursively copies a directory? ;; cp -r ***source*** ***destination***
<!--SR:!2026-06-12,3,250-->

What command moves a file? ;; mv ***source*** ***destination***
<!--SR:!2026-06-12,3,250-->

What command renames a file? ;; mv ***oldname*** ***newname***
<!--SR:!2026-06-10,1,230-->

What command removes a file? ;; rm ***file***
<!--SR:!2026-06-13,4,270-->

What command removes a directory recursively? ;; rm -r ***directory***
<!--SR:!2026-06-12,3,265-->

What command changes file permissions? ;; chmod ***permissions*** ***file***
<!--SR:!2026-06-10,1,230-->

What command removes write permission from a group? ;; chmod g-w ***file***
<!--SR:!2026-06-10,1,230-->

What command removes execute permission from a group? ;; chmod g-x ***file***
<!--SR:!2026-06-10,1,230-->

What command adds read permission to others? ;; chmod o+r ***file***
<!--SR:!2026-06-10,1,230-->

What command displays a file page-by-page? ;; less ***file***
<!--SR:!2026-06-10,1,230-->

What command displays the entire contents of a file? ;; cat ***file***
<!--SR:!2026-06-10,1,230-->

What command displays the first 10 lines of a file? ;; head ***file***
<!--SR:!2026-06-12,3,265-->

What command displays the first 5 lines of a file? ;; head -n 5 ***file***
<!--SR:!2026-06-12,3,265-->

What command displays the last 10 lines of a file? ;; tail ***file***
<!--SR:!2026-06-13,4,270-->

What command displays the last 5 lines of a file? ;; tail -n 5 ***file***
<!--SR:!2026-06-12,3,265-->

What command counts lines, words and bytes in a file? ;; wc ***file***
<!--SR:!2026-06-10,1,225-->

What command counts only lines in a file? ;; wc -l ***file***
<!--SR:!2026-06-10,1,230-->

What command locates the executable path of a command? ;; which ***command***
<!--SR:!2026-06-10,1,230-->

What command gives a short description of a command? ;; whatis ***command***
<!--SR:!2026-06-12,3,250-->

What command opens the manual page of a command? ;; man ***command***
<!--SR:!2026-06-13,4,270-->

What command searches for commands by keyword? ;; apropos ***keyword***
<!--SR:!2026-06-10,1,225-->

What command is equivalent to apropos? ;; man -k ***keyword***
<!--SR:!2026-06-10,1,230-->

What command tells whether something is an alias, builtin or executable? ;; type ***command***
<!--SR:!2026-06-12,3,250-->

What command displays the type of a file? ;; file ***file***
<!--SR:!2026-06-10,1,225-->

What command displays detailed file information? ;; stat ***file***
<!--SR:!2026-06-10,1,230-->

What command shows disk usage? ;; du ***file***
<!--SR:!2026-06-10,1,230-->

What command shows disk usage in human-readable form? ;; du -h ***file***
<!--SR:!2026-06-10,1,225-->

What command creates a symbolic link? ;; ln -s ***source*** ***link***
<!--SR:!2026-06-10,1,225-->

What command creates a hard link? ;; ln ***source*** ***link***
<!--SR:!2026-06-10,1,225-->


What is the root directory in Linux? ;; /
<!--SR:!2026-06-10,1,225-->

What does the root directory represent? ;; The topmost directory from which the entire filesystem hierarchy starts

What does . represent in Linux? ;; The current directory

What does .. represent in Linux? ;; The parent directory

What does ~ represent in Linux? ;; The home directory
<!--SR:!2026-06-12,3,265-->

What does - represent in Linux? ;; The previous working directory

What happens if you use multiple forward slashes in a path? ;; Linux treats them the same as a single forward slash

What is the parent of the root directory? ;; The root directory itself

What are the three categories of Linux permissions? ;; Owner, Group, Others

What are the three basic Linux permissions? ;; Read, Write, Execute
<!--SR:!2026-06-10,1,225-->

What does read permission allow? ;; Viewing the contents of a file

What does write permission allow? ;; Modifying a file or creating/removing files in a directory

What does execute permission allow on a file? ;; Running the file as a program
<!--SR:!2026-06-10,1,225-->

What does execute permission allow on a directory? ;; Entering or traversing the directory

What does rwx mean? ;; Read, write and execute permissions are all granted

What does r-x mean? ;; Read and execute permissions only

What does rw- mean? ;; Read and write permissions only

What numerical value corresponds to read permission? ;; 4

What numerical value corresponds to write permission? ;; 2

What numerical value corresponds to execute permission? ;; 1

What permission does 7 represent? ;; rwx

What permission does 6 represent? ;; rw-

What permission does 5 represent? ;; r-x
<!--SR:!2026-06-10,1,225-->

What permission does 4 represent? ;; r--

What does permission 700 mean? ;; Full permissions for owner and no permissions for group or others

What does permission 755 mean? ;; Full permissions for owner and read-execute permissions for group and others

What does permission 644 mean? ;; Read-write for owner and read-only for group and others

What is a file owner? ;; The user who owns the file

What is a group owner? ;; The group associated with the file

Why do Linux systems have groups? ;; To allow multiple users to share access to files and directories

What does the first character in ls -l output indicate? ;; The file type

What does a - at the beginning of ls -l indicate? ;; A regular file
<!--SR:!2026-06-10,1,225-->

What does d at the beginning of ls -l indicate? ;; A directory
<!--SR:!2026-06-12,3,265-->

What does l at the beginning of ls -l indicate? ;; A symbolic link

What does c at the beginning of ls -l indicate? ;; A character device

What does b at the beginning of ls -l indicate? ;; A block device

What does s at the beginning of ls -l indicate? ;; A socket

What does p at the beginning of ls -l indicate? ;; A named pipe
<!--SR:!2026-06-10,1,225-->

What is a regular file? ;; A normal file such as a text file, script or executable

What is a directory? ;; A container that stores files and other directories
<!--SR:!2026-06-11,2,245-->

What is a symbolic link? ;; A shortcut pointing to another file or directory

What is a character device? ;; A device that transfers data character by character, such as a terminal

What is a block device? ;; A device that transfers data in blocks, such as a hard disk

What is a socket? ;; A special file used for two-way communication between processes
<!--SR:!2026-06-10,1,225-->

What is a named pipe? ;; A special file used for one-way communication between processes

What is an inode? ;; A filesystem data structure that stores metadata about a file

Does an inode store the filename? ;; No

What information does an inode store? ;; Permissions, ownership, timestamps and disk location information

How can two files be identified as hard links? ;; They share the same inode number

What is a hard link? ;; Another filename pointing to the same inode

What is a symbolic link? ;; A separate file that points to another file
<!--SR:!2026-06-10,1,225-->

Do hard links share inode numbers? ;; Yes

Do symbolic links share inode numbers with the original file? ;; No

What happens if one hard link is deleted? ;; The file remains accessible through other hard links

What happens if the original file of a symbolic link is deleted? ;; The symbolic link becomes broken

What is the hard link count shown in ls -l? ;; The number of directory entries pointing to the same inode

Why does every directory contain . ? ;; It is a hard link to itself
<!--SR:!2026-06-10,1,225-->

Why does every directory contain .. ? ;; It is a hard link to its parent directory

What is recursion in file operations? ;; Performing an operation on a directory and all its contents

Why is recursive deletion dangerous? ;; It can delete entire directory trees

What is an alias? ;; A nickname for a command

Why are aliases useful? ;; They save typing and can make commands safer

Why do many Linux users alias rm to rm -i? ;; To prevent accidental file deletion

What is the difference between an option and an argument? ;; Options modify command behavior while arguments specify targets

In ls -l file.txt, what is -l? ;; An option

In ls -l file.txt, what is file.txt? ;; An argument

What is a shell builtin? ;; A command provided directly by the shell

What is an executable command? ;; A command provided by a binary file in the operating system

How can you determine whether a command is an alias, builtin or executable? ;; Using the type command

What is the purpose of a manual page? ;; To provide complete documentation for a command

What is the purpose of the whatis command? ;; To provide a one-line description of a command

What is the purpose of the apropos command? ;; To search for commands by keyword
<!--SR:!2026-06-10,1,225-->

What is the purpose of the which command? ;; To locate the executable path of a command

What is the difference between less and cat? ;; less allows navigation while cat prints everything at once

When is less preferred over cat? ;; For large files

What does head display? ;; The beginning of a file
<!--SR:!2026-06-12,3,265-->

What does tail display? ;; The end of a file

What information does wc provide? ;; Number of lines, words and bytes

What is RAM? ;; Fast primary memory used by running programs
<!--SR:!2026-06-11,2,245-->

What is swap memory? ;; Disk space used as overflow memory when RAM is exhausted

Why is swap slower than RAM? ;; Because disks are much slower than physical memory

What does free -h display? ;; Human-readable memory statistics
<!--SR:!2026-06-10,1,225-->

What does df -h display? ;; Human-readable disk space usage

What does du display? ;; Disk space occupied by a file or directory

Why can disk usage be larger than actual file size? ;; Because files occupy entire filesystem blocks
<!--SR:!2026-06-10,1,225-->

What is a filesystem block? ;; The smallest allocation unit on disk

Can a file occupy part of a block? ;; No

Why does a small file still consume a whole block? ;; Files are allocated in complete blocks

What does stat provide? ;; Detailed file metadata including size, permissions and timestamps

What are timestamps in Linux? ;; Metadata indicating file access, modification and status change times

What does the touch command do to an existing file? ;; Updates its timestamp

What does the touch command do to a nonexistent file? ;; Creates an empty file

What is the /proc filesystem? ;; A virtual filesystem that exposes kernel and process information

Are files in /proc stored on disk? ;; No
<!--SR:!2026-06-10,1,225-->

Why do some files in /proc show size 0 but contain data? ;; They are dynamically generated by the kernel

What information can be found in /proc/cpuinfo? ;; CPU details

What information can be found in /proc/meminfo? ;; Memory details

What information can be found in /proc/version? ;; Kernel version details

What information can be found in /proc/partitions? ;; Disk partition information
<!--SR:!2026-06-10,1,225-->

What is the /sys filesystem? ;; A virtual filesystem exposing hardware and device information

Is /sys newer than /proc for hardware information? ;; Yes

What kind of information can be obtained from /sys? ;; Device, driver and hardware details

Why are /proc and /sys called virtual filesystems? ;; They provide information from memory rather than storing actual files on disk

Why are Linux systems considered multi-user systems? ;; Multiple users can share the same machine and filesystem

Why do Linux files have ownership and permissions? ;; To provide security and controlled access

What causes a Permission Denied error? ;; Lack of required permissions for the attempted operation

Why can ordinary users not modify most system files? ;; They are owned by root and protected by permissions

What is the root user? ;; The superuser with unrestricted access to the system

Why is Linux considered relatively safe for beginners exploring commands? ;; Permissions prevent accidental damage to most system files