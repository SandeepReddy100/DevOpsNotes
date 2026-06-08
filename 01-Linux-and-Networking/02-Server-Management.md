# Server Management: Users, Permissions & VIM

## User & Group Management
Linux relies on strict access control among files and directories.
* **Root User:** Has full access (UID: 0) and uses the `/root/` home directory.
* **Regular User:** Standard permissions (UIDs starting from 1000) and uses `/home/<username>/`.

### Key Commands:
* `su -` : Switch the current user (e.g., to root).
* `useradd` & `userdel` : Add or delete a user.
* `groupadd` & `groupdel` : Add or delete a group.
* `usermod -aG <group>` : Add a user to a specific group.
* `passwd` : Set or change a user's password.
* `id` : Display user ID and group ID information.

## File Permissions
Every file has three types of access: **User (u)**, **Group (g)**, and **Other (o)**.
* `r` (Read) = 4 
* `w` (Write) = 2 
* `x` (Execute) = 1 

### Changing Permissions:
* **chown:** Changes the ownership of a file (`chown <user>:<group> <filepath>`). Use `-R` for recursive changes in a directory.
* **chmod:** Changes the mode/permissions of a file. 
  * *Numeric Example:* `chmod 751 <filepath>` grants read/write/execute (7) to user, read/execute (5) to group, and execute (1) to others.
  * *Symbolic Example:* `chmod ugo+r <filepath>` grants read access to all.

## VIM Editor
VIM is a powerful text editor used in the terminal. Install it using `sudo yum install vim -y`.

### VIM Modes:
1. **Command Mode (Esc):** Default mode for navigation and manipulation.
2. **Insert Mode (`i`):** For typing text.
3. **Extended Mode (`:`):** For saving and quitting.

### Essential VIM Shortcuts:
* `Shift + g` : Go to the last line.
* `gg` : Go to the first line.
* `yy` : Copy line(s).
* `p` : Paste.
* `dd` : Delete/Cut a line (`5dd` deletes 5 lines).
* `u` : Undo.
* `/<text>` : Search for text.
* `:set nu` : Show line numbers.
* `:wq!` : Save and force quit.