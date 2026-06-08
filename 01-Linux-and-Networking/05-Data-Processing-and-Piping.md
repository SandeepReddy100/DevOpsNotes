# Data Processing, Filters, and Redirection in Linux

When managing servers, you will frequently need to search through logs, filter outputs, and redirect data streams. These commands are essential for everyday DevOps tasks.

## 1. File Filters and Text Manipulation
These commands allow you to search, read, and manipulate text within files.

### Searching with `grep` and `find`
* **`grep`**: Used to search for specific text patterns within a file.
  * `grep <text> <filepath>` : Standard search.
  * `grep -i <text> <filepath>` : Case-insensitive search.
  * `grep -v <text> <filepath>` : Invert match (shows lines that *do not* contain the text).
* **`find`**: Used to search for files or directories within a file system.
  * `find <path> -name <filename>` : Finds a file by its exact name.

### Reading and Inspecting Files
* **`less`**: Opens a file for interactive reading (use `?` to search, `q` to quit).
* **`more`**: Reads a file percentage by percentage.
* **`head`**: Outputs the top lines of a file.
  * `head -n 10 <filepath>` : Shows the first 10 lines.
* **`tail`**: Outputs the bottom lines of a file (highly useful for monitoring logs).
  * `tail -n 10 <filepath>` : Shows the last 10 lines.
  * `tail -f <filepath>` : Actively follows the file as new lines are added.

### Advanced Text Processing
* **`cut`**: Extracts specific sections from each line of a file.
  * `cut -d: -f1 <filepath>` : Uses a colon (`:`) as a delimiter and extracts the 1st field.
* **`awk`**: A powerful text pattern scanning and processing language.
  * `awk -F : '{print $1}' <filepath>` : Sets the field separator to `:` and prints the first column.
* **`sed`** (Stream Editor): Used for finding and replacing text.
  * `sed 's/<old>/<new>/g' <filepath>` : Previews the replacement.
  * `sed -i 's/<old>/<new>/g' <filepath>` : Saves (`-i`) the replacement directly into the file.

---

## 2. Input/Output Redirections
By default, commands output their results to the standard display (your screen). Redirection allows you to send that output to files or discard it entirely.

* **`>` (Standard Output / Overwrite):** Writes the output of a command to a file, overwriting existing content.
  * *Example:* `ls > /tmp/info.txt`
* **`>>` (Append):** Adds the output of a command to the end of a file without deleting existing content.
* **`2>` (Standard Error):** Redirects only error messages to a specific location.
* **`/dev/null` (The Black Hole):** A special file that discards any data written to it. Useful for hiding errors.
  * *Example:* `find / -name "test" 2> /dev/null`

---

## 3. Piping (`|`)
Piping takes the standard output of one command and passes it directly as the input to another command. 

* **`wc -l`**: Word count command used to count the number of lines.
* **Piping Example:** `ls -l | wc -l` 
  * *Explanation:* The `ls -l` command lists all files. The pipe (`|`) sends that list to `wc -l`, which counts the total number of files in that directory.

---

## 4. Quick System Monitoring Commands
* **`echo`**: Prints text to the terminal (e.g., `echo "Good morning"`).
* **`free`**: Displays memory (RAM) usage.
* **`df`**: Displays disk partition space and file system usage.
* **`uptime`**: Shows how long the virtual machine or server has been running.
* **`locate`**: A faster alternative to `find`, but it relies on an internal database rather than searching the live filesystem.
  * *Note:* You must install it (`yum install mlocate`) and run `updatedb` to refresh its database before using it to ensure it finds recent files.