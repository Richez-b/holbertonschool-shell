# Shell Basics — Les bases du Shell

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Projet-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Exercices-18-purple)

🌐 **Langue / Language**

🇫🇷 [Français](README.fr.md) | 🇬🇧 [English](README.md)

## 📖 Présentation

Ce projet constitue une introduction aux **commandes fondamentales du Shell Linux**, à la navigation dans le système de fichiers, à la gestion des fichiers et répertoires ainsi qu'à l'utilisation des liens symboliques.

Réalisé dans le cadre de la formation **Holberton School**, il permet d'acquérir les compétences essentielles pour utiliser efficacement un terminal Unix/Linux.

## 🎯 Objectifs pédagogiques

À travers ces exercices, les principales compétences développées sont :

- **Navigation** — Se déplacer dans l'arborescence Linux et identifier le répertoire courant.
- **Gestion des fichiers** — Créer, déplacer, copier et supprimer des fichiers et répertoires.
- **Affichage** — Lister les fichiers et consulter leurs informations.
- **Liens symboliques** — Comprendre et créer des raccourcis vers des fichiers système.
- **Scripts Bash** — Automatiser des opérations simples à l'aide de commandes Shell.

## 📂 Liste des scripts

| Script | Description |
|---|---|
| `0-current_working_directory` | Affiche le chemin absolu du répertoire courant. |
| `1-listit` | Liste le contenu du répertoire courant. |
| `2-bring_me_home` | Permet de revenir au répertoire personnel. |
| `3-listfiles` | Affiche les fichiers au format détaillé. |
| `4-listmorefiles` | Affiche tous les fichiers, y compris les fichiers cachés. |
| `5-listfilesdigitonly` | Affiche les fichiers avec les identifiants numériques des utilisateurs et groupes. |
| `6-firstdirectory` | Crée le répertoire `/tmp/my_first_directory`. |
| `7-movethatfile` | Déplace le fichier `betty` vers `/tmp/my_first_directory`. |
| `8-firstdelete` | Supprime le fichier `betty`. |
| `9-firstdirdeletion` | Supprime le répertoire `/tmp/my_first_directory`. |
| `10-back` | Revient au répertoire précédent. |
| `11-lists` | Liste les fichiers présents dans `.`, `..` et `/boot`. |
| `12-file_type` | Affiche le type du fichier `/tmp/iamafile`. |
| `13-symbolic_link` | Crée un lien symbolique vers `/bin/ls`. |
| `14-copy_html` | Copie les fichiers HTML nouveaux ou modifiés vers le répertoire parent. |
| `15-lets_move` | Déplace les fichiers commençant par une majuscule vers `/tmp/u`. |
| `16-clean_emacs` | Supprime les fichiers se terminant par `~`. |
| `17-tree` | Crée l'arborescence `welcome/to/school`. |

## 💻 Exemple — Exercice 17

L'objectif est de créer une arborescence de répertoires en une seule commande.

```bash
#!/bin/bash
mkdir -p welcome/to/school
```

**Explication :**

- `mkdir` : permet de créer des répertoires.
- `-p` : crée automatiquement les répertoires parents manquants.
- `welcome/to/school` : représente l'arborescence à créer.

**Résultat :**

```text
welcome/
└── to/
    └── school/
```

## ⚙️ Environnement technique

| Technologie | Utilisation |
|---|---|
| **Ubuntu Linux** | Système d'exploitation |
| **Bash** | Interpréteur de commandes |
| **Git** | Gestion des versions |
| **GitHub** | Hébergement du dépôt |

## 🚀 Exécution des scripts

Pour rendre un script exécutable :

```bash
chmod u+x 0-current_working_directory
```

Pour l'exécuter :

```bash
./0-current_working_directory
```

Chaque script Bash commence par :

```bash
#!/bin/bash
```

---

**Dépôt :** `holbertonschool-shell`  
**Répertoire :** `basics`

### 📝 Cette documentation a été rédigée et structurée avec l'aide de l'intelligence artificielle
