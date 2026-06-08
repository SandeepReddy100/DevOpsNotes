# Linux Basics & Core Commands

## Linux Principles & Architecture
Linux follows several core principles that make it powerful for DevOps:
* **Everything is a file**[cite: 143].
* Built using **small, single-purpose programs**[cite: 143].
* The ability to **chain programs** together[cite: 145].
* Configuration data is stored in plain **text files**[cite: 146].

Linux is widely used because it is open-source [cite: 150], highly secure [cite: 152], and built for automation[cite: 149]. The architecture consists of hardware at the base, followed by the Kernel, the Shell, and finally the Application layer[cite: 158].

## Essential Directory Navigation
* `cd /` : Navigate to the root directory[cite: 167].
* `cd ~` : Navigate to the user's home directory.
* `cd /bin` : Contains executable commands for the user[cite: 172].
* `cd /etc` : Contains configuration files[cite: 172].
* `cd /boot` : Contains kernels and bootloaders[cite: 173].
* `pwd` : Print working directory[cite: 119].

## File & Directory Operations
* **Read:** `cat <filepath>` reads the content of a file[cite: 163]. `less` or `more` can be used to read large files interactively[cite: 229, 230].
* **Create:** `mkdir` makes a directory, and `touch` creates an empty file[cite: 179].
* **Copy:** `cp <source> <destination>` copies files. Use `cp -r` for directories[cite: 181, 185].
* **Move/Rename:** `mv <source> <destination>` moves or renames files and directories[cite: 189, 191, 192].
* **Remove:** `rm` removes files. Use `rm -r` to recursively remove directories[cite: 190, 196].

## Filters, Piping & Redirection
* **Grep:** `grep <text> <path>` searches for text. Use `-i` to ignore case, and `-v` to exclude text[cite: 222, 224, 228].
* **Head/Tail:** `head -n` reads the top lines, while `tail -n` reads the bottom lines (useful for log files)[cite: 233, 237, 238].
* **Redirection:** * `>` overwrites a file with command output[cite: 251].
  * `>>` appends command output to a file[cite: 253].
* **Piping (`|`):** Takes the standard output of one command and uses it as the input for another[cite: 275, 277]. Example: `ls | wc -l` counts the number of files[cite: 279, 280].