# Shell — Redirections d'entrées/sorties et filtres

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Projet-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Exercices-23-purple)

🌐 **Langue / Language**

🇫🇷 [Français](README.fr.md) | 🇬🇧 [English](README.md)

## 📖 Présentation du projet

Ce projet fait partie de **Holberton School**.

Il est consacré à la maîtrise des **flux d'entrée/sortie Unix, des opérateurs de redirection, des pipelines et des outils de traitement de texte en ligne de commande**.

L'objectif est de comprendre comment les données circulent entre les commandes, les fichiers et les processus, et comment combiner des outils Unix simples pour effectuer des opérations plus complexes.

Ces notions constituent des bases essentielles pour la programmation Shell, l'administration système et l'automatisation.

## 🎯 Objectifs pédagogiques

Ce projet permet de développer les compétences suivantes :

- **Flux standards** — Comprendre l'entrée standard (`stdin`), la sortie standard (`stdout`) et la sortie d'erreur (`stderr`).
- **Redirections** — Rediriger les résultats des commandes, ajouter du contenu à un fichier et lire des données depuis un fichier.
- **Pipelines** — Relier plusieurs commandes grâce à l'opérateur `|`.
- **Traitement de texte** — Rechercher, filtrer, transformer et organiser des données textuelles.
- **Manipulation de fichiers** — Créer, consulter, modifier et supprimer des fichiers.
- **Combinaison de commandes** — Associer plusieurs outils pour résoudre des problèmes plus complexes.

## 🧠 Concepts fondamentaux

### Les flux standards Unix

Chaque processus Unix utilise généralement trois flux standards :

| Flux | Descripteur | Description |
|---|---|---|
| `stdin` | `0` | Entrée standard — reçoit les données |
| `stdout` | `1` | Sortie standard — affiche les résultats |
| `stderr` | `2` | Sortie d'erreur — affiche les erreurs |

### Les opérateurs de redirection

| Opérateur | Fonction | Exemple |
|---|---|---|
| `>` | Redirige la sortie en écrasant le fichier | `echo "Bonjour" > fichier.txt` |
| `>>` | Ajoute du contenu à la fin d'un fichier | `echo "Monde" >> fichier.txt` |
| `<` | Lit les données depuis un fichier | `wc -l < fichier.txt` |
| `2>` | Redirige les messages d'erreur | `ls inexistant 2> erreurs.txt` |
| `|` | Transmet la sortie d'une commande à une autre | `cat fichier.txt \| grep "root"` |

### Les principaux filtres Unix

| Commande | Utilité |
|---|---|
| `cat` | Affiche ou concatène des fichiers |
| `head` | Affiche les premières lignes |
| `tail` | Affiche les dernières lignes |
| `grep` | Recherche des motifs dans un texte |
| `sort` | Trie les lignes |
| `uniq` | Filtre les doublons consécutifs |
| `wc` | Compte les lignes, mots ou octets |
| `tr` | Remplace ou supprime des caractères |
| `cut` | Extrait des champs spécifiques |
| `find` | Recherche des fichiers et répertoires |
| `rev` | Inverse les caractères de chaque ligne |
| `sed` | Transforme des flux de texte |

## 📂 Structure du projet

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

## 📋 Liste des exercices

| Script | Description |
|---|---|
| `0-hello_world` | Affiche `Hello, World` suivi d'un retour à la ligne. |
| `1-confused_smiley` | Affiche un smiley contenant des caractères spéciaux. |
| `2-hellofile` | Affiche le contenu du fichier `/etc/passwd`. |
| `3-twofiles` | Affiche le contenu de `/etc/passwd` et `/etc/hosts`. |
| `4-lastlines` | Affiche les 10 dernières lignes de `/etc/passwd`. |
| `5-firstlines` | Affiche les 10 premières lignes de `/etc/passwd`. |
| `6-third_line` | Affiche la troisième ligne du fichier `iacta` sans utiliser `sed`. |
| `7-file` | Crée un fichier dont le nom contient des caractères spéciaux et y écrit `Best School`. |
| `8-cwd_state` | Enregistre la liste détaillée du répertoire dans `ls_cwd_content`. |
| `9-duplicate_last_line` | Duplique la dernière ligne du fichier `iacta`. |
| `10-no_more_js` | Supprime tous les fichiers `.js` du répertoire courant et de ses sous-répertoires. |
| `11-directories` | Compte les répertoires et sous-répertoires, sans compter le répertoire courant. |
| `12-newest_files` | Affiche les 10 fichiers les plus récents, triés par date de modification. |
| `13-unique` | Affiche uniquement les mots présents une seule fois, triés alphabétiquement. |
| `14-findthatword` | Affiche les lignes contenant `root` dans `/etc/passwd`. |
| `15-countthatword` | Compte les lignes contenant `bin` dans `/etc/passwd`. |
| `16-whatsnext` | Affiche les lignes contenant `root` et les trois lignes suivantes. |
| `17-hidethatword` | Affiche les lignes ne contenant pas `bin`. |
| `18-letteronly` | Affiche les lignes commençant par une lettre. |
| `19-AZ` | Remplace les caractères `A` et `c` par `Z` et `e`. |
| `20-hi` | Supprime toutes les occurrences des lettres `c` et `C`. |
| `21-reverse` | Inverse l'ordre des caractères de chaque ligne. |
| `22-users_and_homes` | Affiche les utilisateurs et leurs répertoires personnels, triés par nom d'utilisateur. |

## 💻 Exemples pratiques

### Exemple 1 — Afficher la troisième ligne

**Script :** `6-third_line`

```bash
#!/bin/bash
head -n 3 iacta | tail -n 1
```

La première commande récupère les trois premières lignes du fichier, puis la seconde affiche uniquement la dernière de ces trois lignes.

### Exemple 2 — Rechercher un mot dans un fichier

**Script :** `14-findthatword`

```bash
#!/bin/bash
grep "root" /etc/passwd
```

Cette commande recherche toutes les lignes contenant `root`.

### Exemple 3 — Compter les lignes correspondantes

**Script :** `15-countthatword`

```bash
#!/bin/bash
grep -c "bin" /etc/passwd
```

L'option `-c` permet de compter les lignes correspondant au motif recherché.

### Exemple 4 — Inverser du texte

**Script :** `21-reverse`

```bash
#!/bin/bash
rev
```

Exemple :

```text
Entrée : Holberton
Sortie : notrebloH
```

## ⚙️ Prérequis techniques

| Exigence | Spécification |
|---|---|
| Système d'exploitation | Ubuntu 20.04 LTS |
| Interpréteur | Bash |
| Shebang | `#!/bin/bash` |
| Format des fichiers | Fins de ligne Unix |
| Exécution | `chmod u+x` |
| Dépendances | Utilitaires standards Unix |

**Conventions de développement :**

- Tous les scripts commencent par `#!/bin/bash`.
- Chaque fichier se termine par un retour à la ligne.
- Les scripts doivent être exécutables.
- Chaque exercice respecte ses restrictions spécifiques.
- Le code doit rester simple, lisible et facile à maintenir.

## 🚀 Installation et utilisation

### 1. Cloner le dépôt

```bash
git clone https://github.com/<username>/holbertonschool-shell.git
```

### 2. Accéder au projet

```bash
cd holbertonschool-shell/io_redirections_and_filters
```

### 3. Rendre un script exécutable

```bash
chmod u+x 14-findthatword
```

### 4. Exécuter le script

```bash
./14-findthatword
```

### 5. Tester un script avec une entrée standard

```bash
echo "Holberton School" | ./21-reverse
```

Résultat attendu :

```text
loohcS notrebloH
```

## 🧠 Compétences développées

La réalisation de ces exercices permet de renforcer les connaissances suivantes :

- Flux standards Unix et descripteurs de fichiers.
- Redirections d'entrées/sorties et pipelines.
- Recherche de motifs et filtrage de texte.
- Manipulation des fichiers et répertoires.
- Programmation Bash et combinaison de commandes.
- Transformation de données avec les outils Unix.
- Automatisation et efficacité en ligne de commande.

---

**Dépôt :** `holbertonschool-shell`  
**Répertoire :** `io_redirections_and_filters`  
**Projet :** Shell — Redirections d'entrées/sorties et filtres

### 📝 Cette documentation a été rédigée et structurée avec l'aide de l'intelligence artificielle
