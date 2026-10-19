# Shell Basics

This project introduces basic Linux shell commands, file management, directory navigation, permissions, and symbolic links.

## Scripts

- **0-current_working_directory**: Prints the absolute path of the current working directory.
- **1-listit**: Displays the contents of the current directory.
- **2-bring_me_home**: Changes the working directory to the user's home directory.
- **3-listfiles**: Displays the contents of the current directory in long format.
- **4-listmorefiles**: Displays all files, including hidden files, in long format.
- **5-listfilesdigitonly**: Displays all files in long format with numeric user and group IDs.
- **6-firstdirectory**: Creates a directory named `my_first_directory` in `/tmp`.
- **7-movethatfile**: Moves the file `betty` from `/tmp` to `/tmp/my_first_directory`.
- **8-firstdelete**: Deletes the file `betty` from `/tmp/my_first_directory`.
- **9-firstdirdeletion**: Deletes the directory `/tmp/my_first_directory`.
- **10-back**: Changes the working directory to the previous directory.
- **11-lists**: Lists all files, including hidden files, in the current directory, parent directory, and `/boot`, in long format.
- **12-file_type**: Displays the type of the file `/tmp/iamafile`.
- **13-symbolic_link**: Creates a symbolic link named `__ls__` pointing to `/bin/ls`.
- **14-copy_html**: Copies HTML files to the parent directory if they do not exist there or are newer than the existing versions.
- **15-lets_move**: Moves all files beginning with an uppercase letter to `/tmp/u`.
- **16-clean_emacs**: Deletes all files in the current directory whose names end with `~`.
- **17-tree**: Creates the nested directories `welcome/to/school`.

## Requirements

- All scripts are written for Bash.
- All scripts start with `#!/bin/bash`.
- All scripts contain exactly two lines.
- All scripts are executable.
- Scripts are tested on Ubuntu Linux.

## Repository

- **Repository:** `holbertonschool-shell`
- **Directory:** `basics`