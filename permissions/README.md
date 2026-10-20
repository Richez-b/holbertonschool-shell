# Shell — Permissions

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu_20.04-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Project-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Tasks-14-purple)

🌐 **Language / Langue**

🇬🇧 [English](README.md) | 🇫🇷 [Français](README.fr.md)

## 📖 About This Project

This project is part of the **System Engineering & DevOps** curriculum at **Holberton School**.

It focuses on understanding and managing **file permissions, directory access rights, user identities, and group ownership** in Unix/Linux operating systems.

The main objective is to master the Linux multi-user security model and learn how to safely control access to system resources.

These concepts are fundamental to Linux administration, Shell scripting, system security, and DevOps practices.

## 🎯 Learning Objectives

By completing this project, the following skills are developed:

- **User Identification** — Identify the current user and their group memberships.
- **Permission Management** — Understand and modify read, write, and execute permissions.
- **User Classes** — Differentiate between file owners, groups, and other users.
- **Ownership Management** — Change file owners and associated groups.
- **Symbolic and Numeric Modes** — Use symbolic and octal permission notation.
- **Directory Security** — Understand how permissions affect access to directories.
- **Linux Security Fundamentals** — Apply the principle of least privilege.

## 🧠 Core Concepts

### Linux User Classes

Unix/Linux permissions are divided into three categories:

| Class | Symbol | Description |
|---|---|---|
| Owner | `u` | User who owns the file or directory |
| Group | `g` | Users belonging to the file's associated group |
| Others | `o` | All other users |

### Permission Types

| Permission | Symbol | Numeric Value | File Behavior |
|---|---|---|---|
| Read | `r` | `4` | Read file contents |
| Write | `w` | `2` | Modify file contents |
| Execute | `x` | `1` | Execute the file when applicable |

For directories, permissions have different meanings:

- `r` allows listing directory entries.
- `w` allows modifying directory entries when combined with appropriate access.
- `x` allows traversing the directory and accessing known entries.

### Symbolic and Octal Notation

Permissions can be represented using symbolic or numeric notation.

| Octal | Symbolic | Description |
|---|---|---|
| `777` | `rwxrwxrwx` | Full permissions for everyone |
| `755` | `rwxr-xr-x` | Owner full access; others read and execute |
| `750` | `rwxr-x---` | Owner full access; group read and execute |
| `644` | `rw-r--r--` | Owner read/write; others read only |
| `600` | `rw-------` | Owner read/write only |
| `007` | `-------rwx` | Full permissions for others only |

**Example:**

```bash
chmod 755 script.sh
```

This gives the owner read, write, and execute permissions, while the group and others receive read and execute permissions.

### Essential Commands

| Command | Purpose |
|---|---|
| `whoami` | Display the effective username |
| `id` | Display user and group identifiers |
| `groups` | Display group memberships |
| `chmod` | Modify file permission bits |
| `chown` | Change file ownership |
| `chgrp` | Change group ownership |
| `su` | Switch user identity |
| `touch` | Create a file or update timestamps |
| `mkdir` | Create directories |

## 📂 Project Structure

```text
permissions/
│
├── 0-iam_betty
├── 1-who_am_i
├── 2-groups
├── 3-new_owner
├── 4-empty
├── 5-execute
├── 6-multiple_permissions
├── 7-everybody
├── 8-James_Bond
├── 9-John_Doe
├── 10-mirror_permissions
├── 11-directories_permissions
├── 12-directory_permissions
├── 13-change_group
│
├── README.md
└── README.fr.md
```

## 📋 Tasks and Descriptions

| Script | Description |
|---|---|
| `0-iam_betty` | Switches the current user to `betty`. |
| `1-who_am_i` | Prints the effective username of the current user. |
| `2-groups` | Displays the groups to which the current user belongs. |
| `3-new_owner` | Changes the owner of `hello` to `betty`. |
| `4-empty` | Creates an empty file named `hello`. |
| `5-execute` | Adds execute permission for the owner of `hello`. |
| `6-multiple_permissions` | Adds execute permission for the owner and group, and read permission for others. |
| `7-everybody` | Adds execute permission for all user classes. |
| `8-James_Bond` | Sets permissions so only others have full access (`007`). |
| `9-John_Doe` | Sets permissions to `753` (`rwxr-x-wx`). |
| `10-mirror_permissions` | Copies the permission bits of `olleh` to `hello`. |
| `11-directories_permissions` | Adds execute permission to all subdirectories of the current directory for everyone, without changing regular files. |
| `12-directory_permissions` | Creates `my_dir` with permissions `751`. |
| `13-change_group` | Changes the group ownership of `hello` to `school`. |

## 💻 Practical Examples

### Example 1 — Display the Current User

**Script:** `1-who_am_i`

```bash
#!/bin/bash
whoami
```

The `whoami` command displays the effective username of the current process.

### Example 2 — Add Execute Permission

**Script:** `5-execute`

```bash
#!/bin/bash
chmod u+x hello
```

This adds execute permission for the owner without removing existing permissions.

### Example 3 — Give Execute Permission to Everyone

**Script:** `7-everybody`

```bash
#!/bin/bash
chmod a+x hello
```

The `a` symbol represents all user classes: owner, group, and others.

### Example 4 — Copy Permissions from Another File

**Script:** `10-mirror_permissions`

```bash
#!/bin/bash
chmod --reference=olleh hello
```

This copies the permission bits from `olleh` to `hello`.

### Example 5 — Create a Directory with Specific Permissions

**Script:** `12-directory_permissions`

```bash
#!/bin/bash
mkdir -m 751 my_dir
```

This creates `my_dir` with the requested permission mode.

## 🔐 Security Best Practices

Understanding permissions is essential for maintaining a secure Linux environment.

- Apply the **principle of least privilege**.
- Avoid using `chmod 777` unless explicitly required.
- Verify ownership before modifying permissions.
- Be cautious when using recursive permission changes.
- Use administrative privileges only when necessary.
- Check permissions using `ls -l` and `stat`.

**Important:** Some exercises deliberately use unusual or insecure permission configurations for educational purposes. These settings should not be applied blindly to production systems.

## ⚙️ Technical Requirements

| Requirement | Specification |
|---|---|
| Operating System | Ubuntu 20.04 LTS |
| Shell | Bash |
| Shebang | `#!/bin/bash` |
| File Format | Unix-style line endings |
| Executable | `chmod u+x` |
| Dependencies | Standard Unix utilities |

**Coding conventions:**

- Every script starts with `#!/bin/bash`.
- Every file ends with a newline.
- Scripts must have executable permissions.
- Each exercise must respect its specific command restrictions.
- Code should remain simple and readable.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Navigate to the project

```bash
cd holbertonschool-shell/permissions
```

### 3. Make a script executable

```bash
chmod u+x 5-execute
```

### 4. Prepare a test file

```bash
touch hello
```

### 5. Execute the script

```bash
./5-execute
```

### 6. Verify the permissions

```bash
ls -l hello
```

The output will show the updated file permission bits.

## 🧠 Skills Developed

This project strengthens knowledge of:

- Linux user and group management.
- File and directory access control.
- Symbolic and octal permission notation.
- Ownership modification.
- Permission inheritance and directory traversal.
- Shell scripting for system administration.
- Linux security fundamentals.
- Safe resource access management.

---

**Repository:** `holbertonschool-shell`  
**Directory:** `permissions`  
**Project:** Shell — Permissions


### 📝 **AI Disclosure:** This documentation was written and structured with the assistance of artificial intelligence.
