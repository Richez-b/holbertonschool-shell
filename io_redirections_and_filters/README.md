# Shell — I/O Redirections and Filters

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Project-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Tasks-23-purple)

🌐 **Language / Langue**

🇬🇧 [English](README.md) | 🇫🇷 [Français](README.fr.md)

## 📖 About This Project

This project is part of the **System Engineering & DevOps** curriculum at **Holberton School**.

It focuses on mastering **Unix input/output streams, redirection operators, pipelines, and command-line text processing tools**.

The objective is to understand how data flows between commands, files, and processes, and how simple Unix utilities can be combined to perform powerful operations efficiently.

These concepts form an essential foundation for Shell scripting, system administration, and automation.

## 🎯 Learning Objectives

By completing this project, the following skills are developed:

- **Standard Streams** — Understand standard input (`stdin`), standard output (`stdout`), and standard error (`stderr`).
- **I/O Redirections** — Redirect command output, append data to files, and read input from files.
- **Pipelines** — Connect multiple commands using the pipe operator (`|`).
- **Text Processing** — Search, filter, transform, and organize text using Unix utilities.
- **File Manipulation** — Create, inspect, modify, and remove files through Shell commands.
- **Command Composition** — Combine small utilities to solve more complex problems.

## 🧠 Core Concepts

### Standard Input and Output

Unix processes typically interact with three standard streams:

| Stream | Descriptor | Description |
|---|---|---|
| `stdin` | `0` | Standard input — receives data |
| `stdout` | `1` | Standard output — displays normal results |
| `stderr` | `2` | Standard error — displays error messages |

### Redirection Operators

| Operator | Purpose | Example |
|---|---|---|
| `>` | Redirect output and overwrite a file | `echo "Hello" > file.txt` |
| `>>` | Append output to a file | `echo "World" >> file.txt` |
| `<` | Read input from a file | `wc -l < file.txt` |
| `2>` | Redirect error output | `ls missing 2> errors.txt` |
| `|` | Pipe output to another command | `cat file.txt \| grep "root"` |

### Essential Unix Filters

| Command | Purpose |
|---|---|
| `cat` | Display or concatenate file contents |
| `head` | Display the first lines of a file |
| `tail` | Display the last lines of a file |
| `grep` | Search text using patterns |
| `sort` | Sort lines of text |
| `uniq` | Filter adjacent duplicate lines |
| `wc` | Count lines, words, or bytes |
| `tr` | Translate or delete characters |
| `cut` | Extract selected fields |
| `find` | Search for files and directories |
| `rev` | Reverse characters in each line |
| `sed` | Process and transform text streams |

## 📂 Project Structure

```text
io_redirections_and_filters/
│
├── 0-hello_world
├── 1-confused_smiley
├── 2-hellofile
├── 3-twofiles
├── 4-lastlines
├── 5-firstlines
├── 6-third_line
├── 7-file
├── 8-cwd_state
├── 9-duplicate_last_line
├── 10-no_more_js
├── 11-directories
├── 12-newest_files
├── 13-unique
├── 14-findthatword
├── 15-countthatword
├── 16-whatsnext
├── 17-hidethatword
├── 18-letteronly
├── 19-AZ
├── 20-hi
├── 21-reverse
├── 22-users_and_homes
│
├── README.md
└── README.fr.md
```

## 📋 Tasks and Descriptions

| Script | Description |
|---|---|
| `0-hello_world` | Prints `Hello, World` followed by a newline. |
| `1-confused_smiley` | Displays a confused smiley containing special characters. |
| `2-hellofile` | Displays the contents of `/etc/passwd`. |
| `3-twofiles` | Displays the contents of `/etc/passwd` and `/etc/hosts`. |
| `4-lastlines` | Displays the last 10 lines of `/etc/passwd`. |
| `5-firstlines` | Displays the first 10 lines of `/etc/passwd`. |
| `6-third_line` | Displays the third line of the file `iacta` without using `sed`. |
| `7-file` | Creates a file with a special-character filename containing `Best School`. |
| `8-cwd_state` | Saves the long-format directory listing into `ls_cwd_content`. |
| `9-duplicate_last_line` | Duplicates the last line of `iacta`. |
| `10-no_more_js` | Deletes all `.js` files in the current directory and its subdirectories. |
| `11-directories` | Counts directories and subdirectories, excluding the current directory itself. |
| `12-newest_files` | Displays the 10 newest files, ordered by modification time. |
| `13-unique` | Displays words that appear exactly once, sorted alphabetically. |
| `14-findthatword` | Displays lines containing `root` in `/etc/passwd`. |
| `15-countthatword` | Counts lines containing `bin` in `/etc/passwd`. |
| `16-whatsnext` | Displays lines containing `root` and the next three lines. |
| `17-hidethatword` | Displays lines that do not contain `bin`. |
| `18-letteronly` | Displays lines beginning with a letter. |
| `19-AZ` | Replaces uppercase `A` and `c` with `Z` and `e`, respectively. |
| `20-hi` | Removes all occurrences of `c` and `C`. |
| `21-reverse` | Reverses the characters of each input line. |
| `22-users_and_homes` | Displays usernames and home directories, sorted by username. |

## 💻 Practical Examples

### Example 1 — Display the third line

**Script:** `6-third_line`

```bash
#!/bin/bash
head -n 3 iacta | tail -n 1
```

The first command extracts the first three lines, while the second displays only the last of those lines.

### Example 2 — Find a word in a file

**Script:** `14-findthatword`

```bash
#!/bin/bash
grep "root" /etc/passwd
```

This command searches for lines containing `root`.

### Example 3 — Count matching lines

**Script:** `15-countthatword`

```bash
#!/bin/bash
grep -c "bin" /etc/passwd
```

The `-c` option counts matching lines.

### Example 4 — Reverse text

**Script:** `21-reverse`

```bash
#!/bin/bash
rev
```

Example:

```text
Input:  Holberton
Output: notrebloH
```

## ⚙️ Technical Requirements

| Requirement | Specification |
|---|---|
| Operating System | Ubuntu 20.04 LTS |
| Shell | Bash |
| Shebang | `#!/bin/bash` |
| File Format | Unix-style line endings |
| Executable | `chmod u+x` |
| Dependencies | Standard Unix command-line utilities |

**Coding conventions:**

- All scripts must start with `#!/bin/bash`.
- All files must end with a newline.
- Scripts must be executable.
- Each exercise must respect its specific command restrictions.
- Scripts should remain concise, readable, and maintainable.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Navigate to the project

```bash
cd holbertonschool-shell/io_redirections_and_filters
```

### 3. Make a script executable

```bash
chmod u+x 14-findthatword
```

### 4. Run the script

```bash
./14-findthatword
```

### 5. Test a script with standard input

```bash
echo "Holberton School" | ./21-reverse
```

Expected output:

```text
loohcS notrebloH
```

## 🧠 Skills Developed

This project strengthens practical knowledge of:

- Unix standard streams and file descriptors.
- Input/output redirection and pipelines.
- Pattern matching and text filtering.
- File and directory manipulation.
- Shell scripting and command composition.
- Data transformation using standard Unix tools.
- Automation fundamentals and command-line efficiency.

## 🔗 Useful Resources

- [GNU Bash Reference Manual](https://www.gnu.org/software/bash/manual/)
- [GNU Coreutils Documentation](https://www.gnu.org/software/coreutils/manual/)
- [GNU Grep Manual](https://www.gnu.org/software/grep/manual/)
- [Linux Manual Pages](https://man7.org/linux/man-pages/)
- [Holberton School](https://www.holbertonschool.com/)

## 🎓 Academic Context

This project is part of the **Holberton School — System Engineering & DevOps** curriculum.

It introduces essential tools for processing text, managing data streams, and automating operations within a Unix/Linux environment.

---

**Repository:** `holbertonschool-shell`  
**Directory:** `io_redirections_and_filters`  
**Project:** Shell — I/O Redirections and Filters

*Mastering Unix, one command at a time.*
