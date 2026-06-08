# Linux Basics & Core Commands

## Linux Principles & Architecture
Linux follows several core principles that make it powerful for DevOps:
* **Everything is a file**.
* Built using **small, single-purpose programs**.
* The ability to **chain programs** together.
* Configuration data is stored in plain **text files**.

Linux is widely used because it is open-source , highly secure , and built for automation. The architecture consists of hardware at the base, followed by the Kernel, the Shell, and finally the Application layer.

## Essential Directory Navigation
* `cd /` : Navigate to the root directory.
* `cd ~` : Navigate to the user's home directory.
* `cd /bin` : Contains executable commands for the user.
* `cd /etc` : Contains configuration files.
* `cd /boot` : Contains kernels and bootloaders.
* `pwd` : Print working directory.

## File & Directory Operations
* **Read:** `cat <filepath>` reads the content of a file. `less` or `more` can be used to read large files interactively.
* **Create:** `mkdir` makes a directory, and `touch` creates an empty file.
* **Copy:** `cp <source> <destination>` copies files. Use `cp -r` for directories.
* **Move/Rename:** `mv <source> <destination>` moves or renames files and directories.
* **Remove:** `rm` removes files. Use `rm -r` to recursively remove directories.

## Filters, Piping & Redirection
* **Grep:** `grep <text> <path>` searches for text. Use `-i` to ignore case, and `-v` to exclude text.
* **Head/Tail:** `head -n` reads the top lines, while `tail -n` reads the bottom lines (useful for log files).
* **Redirection:** * `>` overwrites a file with command output.
  * `>>` appends command output to a file.
* **Piping (`|`):** Takes the standard output of one command and uses it as the input for another. Example: `ls | wc -l` counts the number of files.