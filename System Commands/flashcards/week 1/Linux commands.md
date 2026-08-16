# ── FILE OPERATIONS ───────────────────────────────────────

How does `mv` differ conceptually from `cp` when working with directories? ;; `mv` moves/renames the directory entry, whereas `cp` must copy the directory contents recursively.

How would you recursively copy a directory to another location? ;; `cp -r <source> <destination>`

How would you remove a directory and everything inside it? ;; `rm -r <directory>` — use with caution because it can delete an entire directory tree.

How would you remove a file while asking for confirmation before deletion? ;; `rm -i <file>`

What does recursion mean in a file operation? ;; Applying the operation to a directory and all of its contents.

Why is recursive deletion particularly dangerous? ;; It can delete an entire directory tree rather than a single file.

# ── FILE CONTENTS / INSPECTION ────────────────────────────

When would you use `less` instead of `cat` to inspect a file? ;; When the file is large and you want to navigate through it interactively.

What is the practical difference between `less` and `more`? ;; `less` supports backward navigation and is generally more feature-rich.

How would you display only the first N lines of a file? only the last N lines of a file? ;; `head -n <N> <file>` . `tail -n <N> <file>`

What information does `wc` provide? ;; Counts such as lines, words, and bytes.

How would you count only the lines in a file? ;; `wc -l <file>`

# ── FILE / FILESYSTEM INFORMATION ─────────────────────────

How would you determine what type of file something actually is? ;; `file <file>`

What does `stat` provide that a simple directory listing may not? ;; Detailed file metadata such as size, permissions, ownership, and timestamps.

What is the difference between `du` and `df`? ;; `du` reports disk usage associated with files/directories; `df` reports available/used space on filesystems.

How would you inspect overall filesystem disk usage in a human-readable form? ;; `df -h`

How would you inspect the disk usage of a file or directory in human-readable form? ;; `du -h <file-or-directory>`

# ── PERMISSIONS ────────────────────────────────────────────

What are the three Linux permission categories? ;; Owner, Group, Others.

Why does Linux represent permissions numerically as 4, 2, and 1? ;; Read = 4, Write = 2, Execute = 1; the values are combined to form an octal permission digit.

What permissions does `7` represent? `6` represent?  `5` represent?;; `rwx` , `rw-` , `r-x` respectively

What does `700` mean? What does `755` mean?  What does `644` mean? ;; Owner has `rwx`; group and others have no permissions. Owner has `rwx`; group and others have `r-x`. Owner has `rw-`; group and others have `r--`. respectively

How would you remove write permission from the group? ;; `chmod g-w <file>`

How would you add read permission for others? ;; `chmod o+r <file>`

If you see `chmod 712 <file>`, how do you interpret the three digits? ;; They specify permissions for owner, group, and others respectively, using `r=4`, `w=2`, `x=1`.

# ── INODES / LINKS ────────────────────────────────────────

What is an inode? ;; A filesystem data structure containing metadata about a file and information used to locate its data blocks.

Does an inode store the filename? ;; No. The filename is associated with a directory entry that points to an inode.

How can you identify two filenames that are hard links to the same file? ;; They point to the same inode number.

What is a hard link? ;; A directory entry that points to the same inode as another directory entry.

What is a symbolic link? ;; A separate file that stores a path to another file or directory.

What is the key inode difference between hard and symbolic links? ;; Hard links point to the same inode; a symbolic link has its own inode and points to a path.

What happens to a file's accessibility when one hard link is deleted? ;; The file remains accessible through any remaining hard links.

What happens when the target of a symbolic link is deleted? ;; The symbolic link becomes broken because its target path no longer resolves.

How would you create a symbolic link? ;; `ln -s <source> <link>`

How would you create a hard link? ;; `ln <source> <link>`

# ── `ls -l` / FILE TYPES ───────────────────────────────────

What does the first character of `ls -l` output tell you? What do `-`, `d`, and `l` at the start of `ls -l` output represent? ;; The file type. Regular file, directory, and symbolic link respectively.

What does the hard-link count in `ls -l` represent? ;; The number of directory entries pointing to the same inode.
# ── VIRTUAL FILESYSTEMS ───────────────────────────────────

What is `/proc`? ;; A virtual filesystem exposing runtime kernel and process information.

Are `/proc` files ordinary files stored on disk? ;; No. Much of their content is generated dynamically by the kernel.

Why can a file in `/proc` show size 0 while still providing information? ;; Its contents are generated dynamically rather than stored as ordinary disk data.

What do numbered directories inside `/proc` represent? ;; Process IDs (PIDs).

What is `/sys`? ;; A virtual filesystem exposing runtime information about hardware, devices, and the kernel.

Why are `/proc` and `/sys` called virtual filesystems? ;; They expose runtime system information rather than representing ordinary files stored on disk.

What information would you look for in `/proc/cpuinfo`, `/proc/meminfo`, and `/proc/version`? ;; CPU details, memory details, and kernel version details respectively.

What does `uname -a` provide? ;; Kernel/system information including the kernel name, version, and system architecture.

# ── COMMANDS / SHELL CONCEPTS ─────────────────────────────

What is the difference between a command option and an argument? ;; An option modifies a command's behavior; an argument specifies what the command operates on.

How can you determine whether a command name refers to an alias, builtin, function, or executable? ;; `type <command>`

How would you locate the executable associated with a command? ;; `which <command>`

How would you get a short description of a command? ;; `whatis <command>`

How would you search command documentation by keyword? ;; `apropos <keyword>` or `man -k <keyword>`

How would you open the manual for a command? ;; `man <command>`

What causes a `Permission denied` error? ;; The current user/process lacks the required permission for the requested operation.

# ── PRACTICAL RECALL ──────────────────────────────────────

You need to move every `.txt` file into a directory called `level1`. What command would you use? ;; `mv *.txt level1`

You want to determine the type of every entry in the current directory. What command would you use? ;; `file *`

You need to set `systemcommands.txt` to permission mode `712`. What command would you use? ;; `chmod 712 systemcommands.txt`

You need to create an empty file named `152.digits`. What command would you use? ;; `touch 152.digits`

# ── EXAM / CONCEPT CHECK ──────────────────────────────────

A hypervisor is software that does what? ;; It creates and runs virtual machines, allowing multiple operating systems to run concurrently while sharing hardware resources.