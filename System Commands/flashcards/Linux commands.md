#Linux 
What command shows the current date and time? ;; date

What command shows the current date in RFC 5322 email format? ;; date -R
<!--SR:!2026-06-13,4,270-->

What command displays the current month's calendar? ;; cal

What command displays a specific month and year calendar? ;; cal <month> <year>

What command displays the calendar in vertical format? ;; ncal

What command shows memory usage? ;; free

What command shows memory usage in human-readable format? ;; free -h
<!--SR:!2026-06-12,3,250-->

What command shows the groups the current user belongs to? ;; groups

What command lists files and directories? ;; ls

What command displays a long listing format? ;; ls -l

What command displays inode numbers? ;; ls -i

What command displays inode numbers and long listing together? ;; ls -li

What command shows information about a directory itself instead of its contents? ;; ls -ld
<!--SR:!2026-06-12,3,250-->

What command shows information about a specific directory in long format? ;; ls -ld <directory>

What command changes to the parent directory? ;; cd ..

What command changes to the home directory? ;; cd ~

What command returns to the previous directory? ;; cd -

What command stays in the current directory? ;; cd .

What command creates a directory? ;; mkdir <directory>

What command creates an empty file? ;; touch <file>

What command updates a file's timestamp? ;; touch <file>

What command copies a file? ;; cp <source> <destination>

What command recursively copies a directory? ;; cp -r <source> <destination>

What command moves a file? ;; mv <source> <destination>

What command renames a file? ;; mv <oldname> <newname>

What command removes a file? ;; rm <file>

What command removes a directory recursively? ;; rm -r <directory>

What command removes an empty directory? ;; rmdir <directory>

What command removes a file interactively with confirmation? ;; rm -i <file>

What command changes file permissions? ;; chmod

What command sets permissions to owner-only access? ;; chmod 700 <file>
<!--SR:!2026-06-10,1,230-->

What command removes write permission from a group? ;; chmod g-w <file>

What command removes execute permission from a group? ;; chmod g-x <file>

What command adds read permission to others? ;; chmod o+r <file>
<!--SR:!2026-06-10,1,230-->

What command displays a file page-by-page? ;; less <file>

How do you quit the less command? ;; q

What command displays the entire contents of a file? ;; cat <file>
<!--SR:!2026-06-10,1,230-->

What command displays the first 10 lines of a file? ;; head <file>

What command displays the first 5 lines of a file? ;; head -n 5 <file>

What command displays the last 10 lines of a file? ;; tail <file>

What command displays the last 5 lines of a file? ;; tail -n 5 <file>
<!--SR:!2026-06-12,3,250-->

What command counts lines, words, and bytes in a file? ;; wc <file>

What command counts only the number of lines in a file? ;; wc -l <file>

What command locates where a command executable is stored? ;; which <command>

What command gives a short description of a command? ;; whatis <command>

What command displays the full manual page of a command? ;; man <command>

What command searches manual pages by keyword? ;; apropos <keyword>

What command is equivalent to apropos? ;; man -k <keyword>
<!--SR:!2026-06-10,1,230-->

What command displays Bash built-in help? ;; help

What command opens the Info documentation browser? ;; info

What command tells whether something is an alias, builtin, or executable? ;; type <command>

What command displays all configured aliases? ;; alias

What command creates an alias? ;; alias name='command'

What command removes an alias? ;; unalias <alias>

What command displays the type of a file? ;; file <file>
<!--SR:!2026-06-10,1,230-->

What command displays detailed file information? ;; stat <file>

What command shows disk usage of a file or directory? ;; du
<!--SR:!2026-06-10,1,230-->

What command shows disk usage in human-readable format? ;; du -h

What command shows mounted partitions and disk space? ;; df
<!--SR:!2026-06-10,1,230-->

What command shows mounted partitions and disk space in human-readable format? ;; df -h

What command displays kernel and system information? ;; uname -a

What command displays CPU information? ;; cat /proc/cpuinfo

What command displays memory information? ;; cat /proc/meminfo

What command displays kernel version information? ;; cat /proc/version

What command displays partition information? ;; cat /proc/partitions

What command creates a symbolic link? ;; ln -s <source> <link>

What command creates a hard link? ;; ln <source> <link>

What command displays file inode numbers? ;; ls -i

What command displays the current directory contents including hidden files? ;; ls -a

What command displays hidden files in long listing format? ;; ls -la

What command displays hidden files with inode numbers and long listing? ;; ls -lia

What command clears the terminal screen? ;; clear

What keyboard shortcut clears the terminal screen? ;; Ctrl + L

What command prints the current working directory? ;; pwd

What command shows who is logged into the system? ;; who

What command shows the current username? ;; whoami

What command displays command location and executable path? ;; which <command>

What command shows whether a command is a shell builtin? ;; type <command>

What command displays the size of files in blocks? ;; ls -s

What command shows detailed file system statistics? ;; stat <file>

What command shows all aliases currently defined? ;; alias

What command removes all contents of a directory recursively? ;; rm -r <directory>
<!--SR:!2026-06-12,3,250-->

What command recursively copies a directory and its contents? ;; cp -r <directory1> <directory2>
<!--SR:!2026-06-10,1,230-->

What command displays the contents of the /proc filesystem CPU information file? ;; cat /proc/cpuinfo

What command displays the contents of the /proc filesystem memory information file? ;; cat /proc/meminfo

What command displays USB device information stored in /sys? ;; cat /sys/.../<file>