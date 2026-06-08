# File Links in Linux

In Linux, alongside standard text files and directories, you can create "links" (similar to shortcuts in Windows). These allow you to reference a file or directory from multiple locations without duplicating the actual data.

## Soft Links (Symbolic Links)
A soft link points to the original file's path. If the original file is deleted, the soft link becomes "broken" or useless.

* **Create a Soft Link:** `ln -s <filepath> <link_name>`
  *(Example: `ln -s /tmp/devops.txt /home/user/devops_shortcut`)*
  
* **Remove a Link:**
  `unlink <link_name>`
  *(This safely removes the link without deleting the original source file).*

*(Note: The `ls -l` command will display soft links with an `l` at the beginning of the permission string, and an arrow `->` pointing to the original file).*