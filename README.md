# Holberton School — Shell
🌐 **Language / Langue**

🇬🇧 [English](README.md) | 🇫🇷 [Français](README.fr.md)

![Bash](https://img.shields.io/badge/Bash-Scripting-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-CLI-121011?style=for-the-badge&logo=gnuterminal&logoColor=white)
![Holberton](https://img.shields.io/badge/Holberton-School-DA291C?style=for-the-badge)

## 📖 About This Repository

This repository contains a collection of **Shell scripting and system engineering projects** developed as part of the **Holberton School curriculum**.

It focuses on building a strong foundation in Unix/Linux environments, command-line operations, Bash scripting, file permissions, and system configuration.

The objective is to progressively develop the technical skills required to navigate, manage, secure, and automate Linux-based systems.

## 🎯 Learning Objectives

Throughout these projects, the following skills are explored:

- **Shell Fundamentals** — Understand how the Unix shell works and interact efficiently with the command-line interface.
- **File System Navigation** — Navigate directories, manage files, and understand the Linux filesystem hierarchy.
- **Permissions & Security** — Manage ownership, access rights, and executable permissions.
- **I/O Redirections & Filters** — Manipulate standard input, output, and error streams while processing text.
- **Environment Variables** — Configure shell environments, initialization files, aliases, and variable expansions.
- **Bash Scripting** — Write executable scripts to automate repetitive tasks and system operations.

## 🗂️ Repository Structure

```text
holbertonschool-shell/
│
├── basics/
│   └── Shell navigation and file management
│
├── permissions/
│   └── File ownership and access permissions
│
├── io_redirections_and_filters/
│   └── Input/output redirections and text processing
│
├── init_files_variables_and_expansions/
│   └── Environment variables and shell expansions
│
└── README.md
```

### 📚 Project Modules

| Module | Description | Key Commands |
|---|---|---|
| **Basics** | Navigation and filesystem operations | `pwd`, `ls`, `cd`, `mkdir`, `cp`, `mv`, `rm` |
| **Permissions** | File permissions and ownership | `chmod`, `chown`, `chgrp`, `id`, `whoami` |
| **I/O Redirections & Filters** | Stream redirection and text manipulation | `echo`, `cat`, `grep`, `head`, `tail`, `sort`, `uniq`, `wc` |
| **Init Files, Variables & Expansions** | Shell configuration and environment management | `printenv`, `export`, `alias`, `source`, `set` |

## ⚙️ Technical Requirements

All scripts follow the project-specific requirements established by Holberton School.

| Requirement | Specification |
|---|---|
| Operating System | Ubuntu 20.04 LTS |
| Shell | Bash |
| Shebang | `#!/bin/bash` |
| File Format | Plain text with Unix-style line endings |
| Executable | Scripts must have executable permissions |
| Code Style | Follow the constraints of each exercise |

**Important conventions:**

- Every Bash script starts with `#!/bin/bash`.
- Every script ends with a newline.
- Scripts should remain simple, readable, and maintainable.
- Commands and utilities must comply with the restrictions of each task.
- Unnecessary comments and dependencies should be avoided.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Navigate to the project

```bash
cd holbertonschool-shell
```

### 3. Choose a module

For example:

```bash
cd basics
```

### 4. Make a script executable

```bash
chmod u+x 0-current_working_directory
```

### 5. Execute the script

```bash
./0-current_working_directory
```

The script will execute using the Bash interpreter specified in its shebang.

## 💻 Example Scripts

### Display the current working directory

```bash
#!/bin/bash
pwd
```

### List files in the current directory

```bash
#!/bin/bash
ls
```

### Display the third line of a file

```bash
#!/bin/bash
head -n 3 iacta | tail -n 1
```

### Count entries in the PATH variable

```bash
#!/bin/bash
printf '%s\n' "$PATH" | tr ':' '\n' | wc -l
```

These examples illustrate fundamental Shell concepts. Individual exercises may impose additional command restrictions.

## 🧠 Skills Developed

By completing these projects, I am strengthening my understanding of:

- Linux system architecture and filesystem organization.
- Command-line productivity and terminal workflows.
- Bash scripting and process execution.
- File permissions and Unix security fundamentals.
- Environment configuration and shell initialization.
- Text processing using standard Unix utilities.
- Automation and scripting best practices.
- Problem-solving within technical constraints.

## 🎓 Academic Context

This repository is part of my learning journey at **Holberton School**, where I am developing practical skills in software engineering, Linux systems, and DevOps fundamentals.

Each directory represents a dedicated learning module, and each script demonstrates the application of a specific Unix or Bash concept.

---

**Holberton School | System Engineering & DevOps**

*Learning Linux, one command at a time.*
