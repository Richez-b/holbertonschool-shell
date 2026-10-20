# Shell — Init Files, Variables and Expansions

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu_20.04-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Project-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Tasks-14-purple)

🌐 **Language / Langue**

🇬🇧 [English](README.md) | 🇫🇷 [Français](README.fr.md)

## 📖 About This Project

This project is part of **Holberton School**.

It focuses on understanding how the **Bash environment is initialized, configured, and customized**, while exploring variables, environment management, arithmetic operations, and Shell expansions.

The main objective is to develop a solid understanding of how Bash processes commands, manages variables, and dynamically evaluates expressions.

These concepts are essential for Shell scripting, Linux system administration, and automation.

## 🎯 Learning Objectives

By completing this project, the following skills are developed:

- **Shell Initialization** — Understand the role of startup files and how Bash loads configuration settings.
- **Local Variables** — Create, modify, and use variables within a Shell session.
- **Environment Variables** — Export variables and understand how they are inherited by child processes.
- **PATH Management** — Configure executable search paths.
- **Shell Expansions** — Use parameter, arithmetic, and brace expansions.
- **Aliases** — Create shortcuts for frequently used commands.
- **Number Manipulation** — Perform calculations and convert values between numerical bases.

## 🧠 Core Concepts

### Shell Initialization Files

Bash uses several configuration files depending on how the Shell is started.

| File | Purpose |
|---|---|
| `/etc/profile` | System-wide initialization for login shells |
| `~/.bash_profile` | User-specific configuration for login shells |
| `~/.profile` | Alternative user login configuration |
| `~/.bashrc` | User configuration for interactive non-login Bash shells |
| `~/.bash_logout` | Commands executed when an interactive login Bash shell exits |

The files that Bash reads depend on whether it is running as a login, interactive, or non-interactive shell.

### Local vs. Environment Variables

| Type | Description | Example |
|---|---|---|
| Local Shell Variable | Available in the current Shell | `BEST="School"` |
| Environment Variable | Exported to child processes | `export BEST="School"` |
| Special Variable | Provides information about Shell execution | `$?`, `$$`, `$#` |

**Example:**

```bash
BEST="School"
echo "$BEST"
```

Exporting the variable:

```bash
export BEST="School"
```

The exported variable becomes available to child processes started from that Shell.

### Special Shell Variables

| Variable | Description |
|---|---|
| `$?` | Exit status of the last command |
| `$$` | Process ID of the current Shell |
| `$#` | Number of positional parameters |
| `$0` | Name used to invoke the Shell or script |
| `$1` | First positional parameter |
| `$@` | All positional parameters |
| `$HOME` | Current user's home directory |
| `$PATH` | Directories searched for executable commands |

### Bash Expansions

| Expansion | Purpose | Example |
|---|---|---|
| Parameter | Retrieve variable values | `$HOME` |
| Arithmetic | Perform integer calculations | `$((5 + 3))` |
| Brace | Generate strings or sequences | `{a,b,c}` |
| Command Substitution | Capture command output | `$(pwd)` |
| Tilde | Expand to the home directory | `~` |

## 📂 Project Structure

```text
init_files_variables_and_expansions/
│
├── 0-alias
├── 1-hello_you
├── 2-path
├── 3-paths
├── 4-global_variables
├── 5-local_variables
├── 6-create_local_variable
├── 7-create_global_variable
├── 8-true_knowledge
├── 9-divide_and_rule
├── 10-love_exponent_the_stars
├── 11-binary_to_decimal
├── 12-combinations
├── 13-print_float
│
├── README.md
└── README.fr.md
```

## 📋 Tasks and Descriptions

| Script | Description |
|---|---|
| `0-alias` | Creates an alias named `ls` that runs `rm *`. |
| `1-hello_you` | Prints `hello` followed by the current Linux username. |
| `2-path` | Appends `/action` to the end of the `PATH` environment variable. |
| `3-paths` | Counts the directory entries listed in `PATH`. |
| `4-global_variables` | Lists environment variables. |
| `5-local_variables` | Lists Shell variables, environment variables, and functions. |
| `6-create_local_variable` | Creates a local variable `BEST` with the value `School`. |
| `7-create_global_variable` | Creates an environment variable `BEST` with the value `School`. |
| `8-true_knowledge` | Prints the result of adding `128` to `TRUE_KNOWLEDGE`. |
| `9-divide_and_rule` | Divides `POWER` by `DIVIDE`. |
| `10-love_exponent_the_stars` | Calculates `BREATH` raised to the power of `LOVE`. |
| `11-binary_to_decimal` | Converts the binary value stored in `BINARY` to decimal. |
| `12-combinations` | Prints all two-letter lowercase combinations except `oo`. |
| `13-print_float` | Prints `NUM` with exactly two decimal places. |

> **Safety note:** Task `0-alias` defines a destructive alias. It must only be tested in a disposable environment, never in a directory containing important files.

## 💻 Practical Examples

### Example 1 — Create a Local Variable

**Script:** `6-create_local_variable`

```bash
#!/bin/bash
BEST="School"
```

This script creates a Shell variable named `BEST`.

### Example 2 — Create an Environment Variable

**Script:** `7-create_global_variable`

```bash
#!/bin/bash
export BEST="School"
```

The `export` command makes the variable available to child processes of the executing Shell.

### Example 3 — Count PATH Entries

**Script:** `3-paths`

```bash
#!/bin/bash
printf '%s\n' "$PATH" | tr ':' '\n' | wc -l
```

This script counts the entries separated by colons in the `PATH` variable.

### Example 4 — Perform Arithmetic

**Script:** `9-divide_and_rule`

```bash
#!/bin/bash
echo $((POWER / DIVIDE))
```

Bash arithmetic expansion performs integer division. The variable `DIVIDE` must not be zero.

### Example 5 — Convert Binary to Decimal

**Script:** `11-binary_to_decimal`

```bash
#!/bin/bash
echo $((2#$BINARY))
```

The `2#` prefix tells Bash to interpret the value as a base-2 integer.

## ⚙️ Technical Requirements

| Requirement | Specification |
|---|---|
| Operating System | Ubuntu 20.04 LTS |
| Shell | Bash |
| Shebang | `#!/bin/bash` |
| File Format | Unix-style line endings |
| Executable | `chmod u+x` |
| Dependencies | Standard Unix utilities and Bash built-ins |

**Coding conventions:**

- Every script starts with `#!/bin/bash`.
- Every file ends with a newline.
- Scripts must have executable permissions.
- Each exercise must respect its specific command restrictions.
- Code should remain concise, readable, and maintainable.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Navigate to the project

```bash
cd holbertonschool-shell/init_files_variables_and_expansions
```

### 3. Make a script executable

```bash
chmod u+x 7-create_global_variable
```

### 4. Execute the script

```bash
./7-create_global_variable
```

### 5. Test variable creation

To test variables in the current Shell session, source the script:

```bash
source ./7-create_global_variable
echo "$BEST"
```

Expected output:

```text
School
```

**Important:** Executing a script with `./script` starts a separate Bash process. Variables defined there do not persist in the parent Shell. Use `source` when you need changes to affect your current session.

## 🧠 Skills Developed

This project strengthens practical knowledge of:

- Bash initialization and configuration files.
- Local and environment variables.
- Variable inheritance and process environments.
- PATH configuration and executable discovery.
- Parameter, arithmetic, and brace expansions.
- Aliases and Shell customization.
- Integer arithmetic and numerical base conversion.
- Bash scripting and automation fundamentals.

---

**Repository:** `holbertonschool-shell`  
**Directory:** `init_files_variables_and_expansions`  
**Project:** Shell — Init Files, Variables and Expansions

### 📝 This documentation was written and structured with the assistance of artificial intelligence
