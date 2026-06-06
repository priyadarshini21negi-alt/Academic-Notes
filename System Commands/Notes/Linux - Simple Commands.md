#Linux
#  Directory Shortcuts 
1. Current directory ;; `cd .`
<!--SR:!2026-06-07,4,270-->
2. parent directory - `cd ..`
3. Home directory ;; `cd ~`
<!--SR:!2026-06-07,4,270-->
4. Previous directory ;; `cd -`
<!--SR:!2026-06-07,4,270--> 
5. Multiple slashes are treated as same? ;; Yes
<!--SR:!2026-06-10,4,276-->
6. Root is its own parent :- 
	1. ![[Pasted image 20260605205811.png]] 

# Useful System Information Command 
1. Date - `date`
2. Date in RFC email format ;; `date -R`
3. Calendar ;; `cal`
<!--SR:!2026-06-10,4,276-->
4. Specific month (August 1946) ;; `cal August 1946` or `cal 8 1946`
<!--SR:!2026-06-09,3,256-->
5. Vertical calendar ;; `ncal`

# Memory Statistics 
1. Show RAM usage ;; `free`
<!--SR:!2026-06-07,1,236-->
2. Better version to show RAM usage (human readable format );; `free -h`
3. **Swap Memory?** ;; Swap is a disk space used as Emergency memory when RAM is full. RAM -> fast ; Swap-> Slow. If Swap usage is 0, that's good
<!--SR:!2026-06-07,1,236-->
4. What command displays the groups a user belongs to? ;; groups
<!--SR:!2026-06-09,3,256-->
	What does membership in the `sudo` group allow?;; Administrative privileges
	Give examples of common Linux groups.;; student, sudo, docker
<!--SR:!2026-06-07,1,236-->
# About `ls`
1. *Understanding `ls -l`* 
		Example:
`drwxr-xr-x 2 user group 4096 Nov 25 Documents`
What does the first character of `drwxr-xr-x` represent?;; File type

What do the next 9 characters represent? ;; Permissions

What does `user` represent in `ls -l` output?;;Owner
<!--SR:!2026-06-07,1,236-->

What does `group` represent in `ls -l` output?;;Group ownership
<!--SR:!2026-06-07,1,236-->

What does `4096` represent in `ls -l` output?;;Size in bytes
<!--SR:!2026-06-07,1,236-->


6. View contents of Another Directory ;; `ls -l filename `
<!--SR:!2026-06-07,1,236-->
7. View info about directory itself ;; `ls -ld filename` 
		Without `-d`, Linux enters the directory.
		With `-d`, Linux shows information about the directory object itself. 
8. Show Inode + Long listing ;; `ls -ldi filename (or) ls -idl level1 (or) ls -lid level1` 
	- Shows : inode number, permissions, ownership, size
9. Long Options : ![[Pasted image 20260605210535.png]] 
# Commands for Reading Text Files 
- Best command for reading text files. Why? ;; `less file.txt` Features : Scroll up/down, Search, Quit anytime with `q` 
- Prints entire file immediately ;; `cat file.txt` Good for : Small files. not huge cuz everything floods the screen 
- Older version of `less` ;; `more file.txt` Page-by-Page viewing.
<!--SR:!2026-06-10,4,276-->
- Beginning of a file. Default lines? Custom number? ;; `head` file.txt . 10 lines. `head -n 5 file.txt` 
- end of file. Default lines? Custom lines? ;; `tail file.txt` . 10 lines. `tail -n 5 file.txt` 
# Count Lines, Words, Characters 
- Counting lines, words, characters. Output? ;; `wc file.txt` `27 97 581 file.txt` (lines, words, bytes)
<!--SR:!2026-06-07,1,236-->
- Only 1 line count ;; `wc -l file.txt`
<!--SR:!2026-06-09,3,256-->
- Finding commands. To tell location. Output? ;; `which ls` . `/usr/bin/ls`
<!--SR:!2026-06-07,1,236-->
- What does a command do? Output? ;; `whatis ls` . `ls - list directory contents`
<!--SR:!2026-06-07,1,236-->
- Full documentation / complete manual ;; `man ls`
<!--SR:!2026-06-07,1,236-->

# Discovering New Commands 
(One of linux's hidden superpower) 
- Shows all commands related to "who". ;; `apropos who` / `man -k who`
- Shows bash built-in commands. Some commands come from linux and some from bash ;; `help` 
- Text-based documentation browser. Think Wikipedia for installed linux commands inside your terminal ;; `info` 
- where a command comes from. ;; `type ls` 

# Aliases 
- Nickname for a command ;; Alias 
- Alias command example ;; `alias ll='ls -l'`