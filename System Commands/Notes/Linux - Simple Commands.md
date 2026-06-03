#Linux
#  Directory Shortcuts 
1. Current directory ;; `cd .`
<!--SR:!2026-06-07,4,270-->
2. parent directory - `cd ..`
3. Home directory ;; `cd ~`
<!--SR:!2026-06-07,4,270-->
4. Previous directory ;; `cd -`
<!--SR:!2026-06-07,4,270-->

# Useful System Information Command 
1. Date - `date`
2. Date in RFC email format ;; `date -R`
3. Calendar ;; `cal` 
4. Specific month (August 1946) ;; `cal August 1946` or `cal 8 1946` 
5. Vertical calendar ;; `ncal`

# Memory Statistics 
1. Show RAM usage ;; `free` 
2. Better version to show RAM usage (human readable format );; `free -h`
3. **Swap Memory?** ;; Swap is a disk space used as Emergency memory when RAM is full. RAM -> fast ; Swap-> Slow. If Swap usage is 0, that's good 
4. What command displays the groups a user belongs to? ;; groups
	What does membership in the `sudo` group allow?;; Administrative privileges
	Give examples of common Linux groups.;; student, sudo, docker
5. *Understanding `ls -l`* 
		Example:
`drwxr-xr-x 2 user group 4096 Nov 25 Documents`
What does the first character of `drwxr-xr-x` represent?;; File type

What do the next 9 characters represent? ;; Permissions

What does `user` represent in `ls -l` output?;;Owner

What does `group` represent in `ls -l` output?;;Group ownership

What does `4096` represent in `ls -l` output?;;Size in bytes 
