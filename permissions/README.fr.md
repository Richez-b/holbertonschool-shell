# Shell — Permissions et droits d'accès

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu_20.04-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Projet-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Exercices-14-purple)

🌐 **Langue / Language**

🇫🇷 [Français](README.fr.md) | 🇬🇧 [English](README.md)

## 📖 Présentation du projet

Ce projet fait partie du cursus **System Engineering & DevOps** de **Holberton School**.

Il est consacré à la compréhension et à la gestion des **permissions de fichiers, des droits d'accès aux répertoires, des identités utilisateurs et de l'appartenance aux groupes** dans les systèmes Unix/Linux.

L'objectif principal est de maîtriser le modèle de sécurité multi-utilisateur de Linux et d'apprendre à contrôler les accès aux ressources système.

Ces concepts sont fondamentaux pour l'administration Linux, la programmation Shell, la sécurité informatique et les pratiques DevOps.

## 🎯 Objectifs pédagogiques

Ce projet permet de développer les compétences suivantes :

- **Identification des utilisateurs** — Identifier l'utilisateur courant et ses groupes.
- **Gestion des permissions** — Comprendre et modifier les droits de lecture, d'écriture et d'exécution.
- **Catégories d'utilisateurs** — Différencier le propriétaire, le groupe et les autres utilisateurs.
- **Gestion des propriétaires** — Modifier le propriétaire d'un fichier et son groupe associé.
- **Notations symboliques et numériques** — Utiliser les permissions sous forme symbolique ou octale.
- **Sécurité des répertoires** — Comprendre l'impact des permissions sur l'accès aux dossiers.
- **Fondamentaux de sécurité Linux** — Appliquer le principe du moindre privilège.

## 🧠 Concepts fondamentaux

### Les catégories d'utilisateurs

Les permissions Unix/Linux sont organisées en trois catégories :

| Catégorie | Symbole | Description |
|---|---|---|
| Propriétaire | `u` | Utilisateur propriétaire du fichier |
| Groupe | `g` | Utilisateurs appartenant au groupe associé |
| Autres | `o` | Tous les autres utilisateurs |

### Les types de permissions

| Permission | Symbole | Valeur | Comportement sur un fichier |
|---|---|---|---|
| Lecture | `r` | `4` | Lire le contenu |
| Écriture | `w` | `2` | Modifier le contenu |
| Exécution | `x` | `1` | Exécuter le fichier lorsque cela est applicable |

Pour les répertoires, ces permissions ont un fonctionnement différent :

- `r` permet de consulter la liste des entrées.
- `w` permet de modifier les entrées lorsque les autres droits nécessaires sont présents.
- `x` permet de traverser le répertoire et d'accéder aux entrées connues.

### Notations symboliques et octales

Les permissions peuvent être représentées sous forme symbolique ou numérique.

| Octal | Symbolique | Description |
|---|---|---|
| `777` | `rwxrwxrwx` | Tous les droits pour tous |
| `755` | `rwxr-xr-x` | Tous les droits pour le propriétaire, lecture et exécution pour les autres |
| `750` | `rwxr-x---` | Tous les droits pour le propriétaire, lecture et exécution pour le groupe |
| `644` | `rw-r--r--` | Lecture/écriture pour le propriétaire, lecture pour les autres |
| `600` | `rw-------` | Lecture/écriture uniquement pour le propriétaire |
| `007` | `-------rwx` | Tous les droits uniquement pour les autres |

**Exemple :**

```bash
chmod 755 script.sh
```

Cette commande attribue les permissions de lecture, d'écriture et d'exécution au propriétaire, et les permissions de lecture et d'exécution au groupe et aux autres utilisateurs.

### Commandes essentielles

| Commande | Utilité |
|---|---|
| `whoami` | Affiche le nom de l'utilisateur effectif |
| `id` | Affiche les identifiants utilisateur et groupe |
| `groups` | Affiche les groupes de l'utilisateur |
| `chmod` | Modifie les permissions |
| `chown` | Change le propriétaire |
| `chgrp` | Change le groupe propriétaire |
| `su` | Change d'identité utilisateur |
| `touch` | Crée un fichier ou actualise ses dates |
| `mkdir` | Crée des répertoires |

## 📂 Structure du projet

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

## 📋 Liste des exercices

| Script | Description |
|---|---|
| `0-iam_betty` | Permet de changer d'utilisateur pour devenir `betty`. |
| `1-who_am_i` | Affiche le nom de l'utilisateur effectif. |
| `2-groups` | Affiche les groupes auxquels appartient l'utilisateur courant. |
| `3-new_owner` | Change le propriétaire du fichier `hello` en `betty`. |
| `4-empty` | Crée un fichier vide nommé `hello`. |
| `5-execute` | Ajoute la permission d'exécution au propriétaire de `hello`. |
| `6-multiple_permissions` | Ajoute l'exécution au propriétaire et au groupe, et la lecture aux autres. |
| `7-everybody` | Ajoute l'exécution à toutes les catégories d'utilisateurs. |
| `8-James_Bond` | Attribue tous les droits uniquement aux autres utilisateurs (`007`). |
| `9-John_Doe` | Définit les permissions sur `753` (`rwxr-x-wx`). |
| `10-mirror_permissions` | Copie les permissions du fichier `olleh` vers `hello`. |
| `11-directories_permissions` | Ajoute l'exécution à tous les sous-répertoires pour tous, sans modifier les fichiers ordinaires. |
| `12-directory_permissions` | Crée le répertoire `my_dir` avec les permissions `751`. |
| `13-change_group` | Change le groupe propriétaire du fichier `hello` en `school`. |

## 💻 Exemples pratiques

### Exemple 1 — Afficher l'utilisateur courant

**Script :** `1-who_am_i`

```bash
#!/bin/bash
whoami
```

La commande `whoami` affiche le nom de l'utilisateur effectif du processus courant.

### Exemple 2 — Ajouter la permission d'exécution

**Script :** `5-execute`

```bash
#!/bin/bash
chmod u+x hello
```

Cette commande ajoute la permission d'exécution au propriétaire sans supprimer les permissions existantes.

### Exemple 3 — Autoriser l'exécution pour tous

**Script :** `7-everybody`

```bash
#!/bin/bash
chmod a+x hello
```

Le symbole `a` représente toutes les catégories d'utilisateurs : propriétaire, groupe et autres.

### Exemple 4 — Copier les permissions d'un fichier

**Script :** `10-mirror_permissions`

```bash
#!/bin/bash
chmod --reference=olleh hello
```

Cette commande copie les permissions de `olleh` vers `hello`.

### Exemple 5 — Créer un répertoire avec des permissions spécifiques

**Script :** `12-directory_permissions`

```bash
#!/bin/bash
mkdir -m 751 my_dir
```

Cette commande crée le répertoire `my_dir` avec les permissions demandées.

## 🔐 Bonnes pratiques de sécurité

La compréhension des permissions est essentielle pour maintenir un environnement Linux sécurisé.

- Appliquer le **principe du moindre privilège**.
- Éviter `chmod 777` sauf nécessité explicite.
- Vérifier les propriétaires avant de modifier les permissions.
- Être prudent avec les modifications récursives.
- Utiliser les privilèges administrateur uniquement lorsque nécessaire.
- Vérifier les droits avec `ls -l` et `stat`.

**Important :** certains exercices utilisent volontairement des configurations inhabituelles ou peu sécurisées à des fins pédagogiques. Elles ne doivent pas être appliquées sans précaution à des systèmes en production.

## ⚙️ Prérequis techniques

| Exigence | Spécification |
|---|---|
| Système d'exploitation | Ubuntu 20.04 LTS |
| Interpréteur | Bash |
| Shebang | `#!/bin/bash` |
| Format des fichiers | Fins de ligne Unix |
| Exécution | `chmod u+x` |
| Dépendances | Utilitaires Unix standards |

**Conventions de développement :**

- Chaque script commence par `#!/bin/bash`.
- Chaque fichier se termine par un retour à la ligne.
- Les scripts doivent être exécutables.
- Chaque exercice respecte ses restrictions spécifiques.
- Le code doit rester simple et lisible.

## 🚀 Installation et utilisation

### 1. Cloner le dépôt

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Accéder au projet

```bash
cd holbertonschool-shell/permissions
```

### 3. Rendre un script exécutable

```bash
chmod u+x 5-execute
```

### 4. Préparer un fichier de test

```bash
touch hello
```

### 5. Exécuter le script

```bash
./5-execute
```

### 6. Vérifier les permissions

```bash
ls -l hello
```

Le résultat affiche les permissions du fichier après modification.

## 🧠 Compétences développées

Ce projet permet d'approfondir les connaissances suivantes :

- Gestion des utilisateurs et groupes Linux.
- Contrôle des accès aux fichiers et répertoires.
- Notations symboliques et octales.
- Modification des propriétaires et groupes.
- Permissions et parcours des répertoires.
- Programmation Shell pour l'administration système.
- Principes fondamentaux de sécurité Linux.
- Gestion sécurisée des ressources système.

---

**Dépôt :** `holbertonschool-shell`  
**Répertoire :** `permissions`  
**Projet :** Shell — Permissions et droits d'accès


📝 **Mention IA :** Cette documentation a été rédigée et structurée avec l'aide de l'intelligence artificielle.
