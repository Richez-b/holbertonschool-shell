# Holberton School — Shell

![Bash](https://img.shields.io/badge/Bash-Scripting-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-CLI-121011?style=for-the-badge&logo=gnuterminal&logoColor=white)

🇫🇷 **[Français](README.fr.md)** | 🇬🇧 **[English](README.md)**

## 📖 Présentation

Ce dépôt regroupe les projets de **programmation Shell** réalisés dans le cadre de ma formation à **Holberton School**.

Il permet d'acquérir des bases solides dans l'utilisation des systèmes Unix/Linux, la manipulation du terminal, les scripts Bash, la gestion des permissions et la configuration de l'environnement système.

L'objectif est de développer progressivement les compétences nécessaires pour **naviguer, administrer, sécuriser et automatiser des systèmes Linux**.

## 🎯 Objectifs pédagogiques

Les projets abordent plusieurs compétences fondamentales :

- **Fondamentaux du Shell** — Comprendre le fonctionnement du Shell Unix et utiliser efficacement le terminal.
- **Navigation dans le système de fichiers** — Explorer les répertoires, gérer les fichiers et comprendre l'arborescence Linux.
- **Permissions et sécurité** — Gérer les droits d'accès, les propriétaires et les permissions d'exécution.
- **Redirections et filtres** — Manipuler les flux d'entrée et de sortie et traiter des données textuelles.
- **Variables d'environnement** — Configurer les fichiers d'initialisation, les alias et les variables Shell.
- **Scripts Bash** — Écrire des scripts exécutables pour automatiser les tâches répétitives.

## 🗂️ Structure du dépôt

```text
holbertonschool-shell/
│
├── basics/
│   └── Navigation et gestion des fichiers
│
├── permissions/
│   └── Permissions et droits d'accès
│
├── io_redirections_and_filters/
│   └── Redirections et traitement de texte
│
├── init_files_variables_and_expansions/
│   └── Variables d'environnement et expansions
│
├── README.md
└── README.fr.md
```

### 📚 Modules

| Module | Description | Commandes principales |
|---|---|---|
| **Basics** | Navigation et gestion du système de fichiers | `pwd`, `ls`, `cd`, `mkdir`, `cp`, `mv`, `rm` |
| **Permissions** | Gestion des permissions et des propriétaires | `chmod`, `chown`, `chgrp`, `id`, `whoami` |
| **I/O Redirections & Filters** | Redirections et manipulation de texte | `echo`, `cat`, `grep`, `head`, `tail`, `sort`, `uniq`, `wc` |
| **Init Files, Variables & Expansions** | Configuration du Shell et variables d'environnement | `printenv`, `export`, `alias`, `source`, `set` |

## ⚙️ Prérequis techniques

Tous les scripts respectent les exigences propres aux projets de Holberton School.

| Exigence | Spécification |
|---|---|
| Système d'exploitation | Ubuntu 20.04 LTS |
| Interpréteur | Bash |
| Shebang | `#!/bin/bash` |
| Format | Texte brut avec fins de ligne Unix |
| Exécution | Permissions exécutables obligatoires |
| Style | Respect des contraintes de chaque exercice |

**Conventions :**

- Chaque script Bash commence par `#!/bin/bash`.
- Chaque fichier se termine par un retour à la ligne.
- Les scripts doivent être simples, lisibles et faciles à maintenir.
- Les commandes utilisées respectent les restrictions de chaque exercice.
- Les commentaires et dépendances inutiles sont évités.

## 🚀 Démarrage rapide

### 1. Cloner le dépôt

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Accéder au projet

```bash
cd holbertonschool-shell
```

### 3. Choisir un module

```bash
cd basics
```

### 4. Rendre un script exécutable

```bash
chmod u+x 0-current_working_directory
```

### 5. Exécuter le script

```bash
./0-current_working_directory
```

## 💻 Exemples de scripts

### Afficher le répertoire courant

```bash
#!/bin/bash
pwd
```

### Lister les fichiers

```bash
#!/bin/bash
ls
```

### Afficher la troisième ligne d'un fichier

```bash
#!/bin/bash
head -n 3 iacta | tail -n 1
```

### Compter les entrées de PATH

```bash
#!/bin/bash
printf '%s\n' "$PATH" | tr ':' '\n' | wc -l
```

Ces exemples illustrent les concepts fondamentaux du Shell. Certains exercices imposent des restrictions supplémentaires.

## 🧠 Compétences développées

La réalisation de ces projets me permet de renforcer mes connaissances dans les domaines suivants :

- Architecture Linux et organisation du système de fichiers.
- Utilisation avancée du terminal.
- Programmation Bash et exécution de scripts.
- Permissions Unix et principes de sécurité.
- Configuration des environnements Shell.
- Traitement de texte avec les outils Unix.
- Automatisation des tâches système.
- Résolution de problèmes sous contraintes techniques.

---

**Holberton School | Ingénierie Système & DevOps**

*Apprendre Linux, une commande à la fois.*
