# Server Management: Users, Permissions & VIM

## User & Group Management
Linux relies on strict access control among files and directories[cite: 293].
* **Root User:** Has full access (UID: 0) and uses the `/root/` home directory[cite: 293].
* **Regular User:** Standard permissions (UIDs starting from 1000) and uses `/home/<username>/`[cite: 293].

### Key Commands:
* `su -` : Switch the current user (e.g., to root)[cite: 302, 304].
* `useradd` & `userdel` : Add or delete a user[cite: 295, 297].
* `groupadd` & `groupdel` : Add or delete a group[cite: 299, 300].
* `usermod -aG <group>` : Add a user to a specific group[cite: 309].
* `passwd` : Set or change a user's password[cite: 310, 314].
* `id` : Display user ID and group ID information[cite: 312, 315].

## File Permissions
Every file has three types of access: **User (u)**, **Group (g)**, and **Other (o)**[cite: 332, 335, 338, 369].
* `r` (Read) = 4 [cite: 318, 364]
* `w` (Write) = 2 [cite: 323, 364]
* `x` (Execute) = 1 [cite: 328, 365]

### Changing Permissions:
* **chown:** Changes the ownership of a file (`chown <user>:<group> <filepath>`)[cite: 347, 356]. Use `-R` for recursive changes in a directory[cite: 353, 358].
* **chmod:** Changes the mode/permissions of a file[cite: 348, 351]. 
  * *Numeric Example:* `chmod 751 <filepath>` grants read/write/execute (7) to user, read/execute (5) to group, and execute (1) to others[cite: 368].
  * *Symbolic Example:* `chmod ugo+r <filepath>` grants read access to all[cite: 371, 377].

## VIM Editor
VIM is a powerful text editor used in the terminal[cite: 202]. Install it using `sudo yum install vim -y`[cite: 203].

### VIM Modes:
1. **Command Mode (Esc):** Default mode for navigation and manipulation[cite: 204].
2. **Insert Mode (`i`):** For typing text[cite: 205].
3. **Extended Mode (`:`):** For saving and quitting[cite: 206].

### Essential VIM Shortcuts:
* `Shift + g` : Go to the last line[cite: 207].
* `gg` : Go to the first line[cite: 207].
* `yy` : Copy line(s)[cite: 207].
* `p` : Paste[cite: 207].
* `dd` : Delete/Cut a line (`5dd` deletes 5 lines)[cite: 207].
* `u` : Undo[cite: 207].
* `/<text>` : Search for text[cite: 207].
* `:set nu` : Show line numbers[cite: 207].
* `:wq!` : Save and force quit[cite: 207, 209].