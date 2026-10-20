# Shell — Fichiers d'initialisation, variables et expansions

![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash&logoColor=white)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu_20.04-E95420?logo=ubuntu&logoColor=white)
![Holberton](https://img.shields.io/badge/Projet-Holberton-007ACC)
![Tasks](https://img.shields.io/badge/Exercices-14-purple)

🌐 **Langue / Language**

🇫🇷 [Français](README.fr.md) | 🇬🇧 [English](README.md)

## 📖 Présentation du projet

Ce projet fait partie du cursus de **Holberton School**.

Il est consacré à la compréhension du **fonctionnement, de l'initialisation et de la configuration de l'environnement Bash**, ainsi qu'à la manipulation des variables, aux opérations arithmétiques et aux mécanismes d'expansion du Shell.

L'objectif principal est d'acquérir une compréhension solide de la manière dont Bash interprète les commandes, gère les variables et évalue dynamiquement les expressions.

Ces connaissances sont essentielles pour la programmation Shell, l'administration Linux et l'automatisation.

## 🎯 Objectifs pédagogiques

Ce projet permet de développer les compétences suivantes :

- **Initialisation du Shell** — Comprendre le rôle des fichiers de configuration et leur chargement par Bash.
- **Variables locales** — Créer, modifier et utiliser des variables dans une session Shell.
- **Variables d'environnement** — Exporter des variables et comprendre leur transmission aux processus enfants.
- **Gestion de PATH** — Configurer les chemins de recherche des commandes exécutables.
- **Expansions Bash** — Utiliser les expansions de paramètres, arithmétiques et d'accolades.
- **Alias** — Créer des raccourcis pour les commandes fréquemment utilisées.
- **Manipulation numérique** — Effectuer des calculs et convertir des nombres entre différentes bases.

## 🧠 Concepts fondamentaux

### Fichiers d'initialisation du Shell

Bash utilise différents fichiers de configuration selon son mode de démarrage.

| Fichier | Rôle |
|---|---|
| `/etc/profile` | Configuration globale des Shells de connexion |
| `~/.bash_profile` | Configuration personnelle d'un Shell de connexion |
| `~/.profile` | Configuration alternative de connexion |
| `~/.bashrc` | Configuration des Shells Bash interactifs sans connexion |
| `~/.bash_logout` | Commandes exécutées à la fermeture d'un Shell Bash interactif de connexion |

Les fichiers chargés dépendent du mode d'exécution du Shell : connexion, interactif ou non interactif.

### Variables locales et variables d'environnement

| Type | Description | Exemple |
|---|---|---|
| Variable locale | Accessible dans le Shell courant | `BEST="School"` |
| Variable d'environnement | Transmise aux processus enfants | `export BEST="School"` |
| Variable spéciale | Fournit des informations sur l'exécution du Shell | `$?`, `$$`, `$#` |

**Exemple :**

```bash
BEST="School"
echo "$BEST"
```

Pour exporter la variable :

```bash
export BEST="School"
```

La variable exportée devient accessible aux processus enfants lancés depuis ce Shell.

### Variables spéciales Bash

| Variable | Description |
|---|---|
| `$?` | Code de retour de la dernière commande |
| `$$` | Identifiant du processus Shell courant |
| `$#` | Nombre de paramètres positionnels |
| `$0` | Nom utilisé pour lancer le Shell ou le script |
| `$1` | Premier paramètre positionnel |
| `$@` | Ensemble des paramètres positionnels |
| `$HOME` | Répertoire personnel de l'utilisateur |
| `$PATH` | Répertoires dans lesquels les commandes exécutables sont recherchées |

### Expansions Bash

| Expansion | Fonction | Exemple |
|---|---|---|
| Paramètre | Récupère la valeur d'une variable | `$HOME` |
| Arithmétique | Effectue des calculs entiers | `$((5 + 3))` |
| Accolades | Génère des chaînes ou séquences | `{a,b,c}` |
| Substitution de commande | Récupère la sortie d'une commande | `$(pwd)` |
| Tilde | Représente le répertoire personnel | `~` |

## 📂 Structure du projet

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

## 📋 Liste des exercices

| Script | Description |
|---|---|
| `0-alias` | Crée un alias `ls` exécutant la commande `rm *`. |
| `1-hello_you` | Affiche `hello` suivi du nom de l'utilisateur connecté. |
| `2-path` | Ajoute `/action` à la fin de la variable d'environnement `PATH`. |
| `3-paths` | Compte les entrées de répertoires présentes dans `PATH`. |
| `4-global_variables` | Affiche les variables d'environnement. |
| `5-local_variables` | Affiche les variables du Shell, les variables d'environnement et les fonctions. |
| `6-create_local_variable` | Crée une variable locale `BEST` contenant `School`. |
| `7-create_global_variable` | Crée une variable d'environnement `BEST` contenant `School`. |
| `8-true_knowledge` | Affiche le résultat de l'addition de `128` à `TRUE_KNOWLEDGE`. |
| `9-divide_and_rule` | Divise `POWER` par `DIVIDE`. |
| `10-love_exponent_the_stars` | Calcule `BREATH` élevé à la puissance `LOVE`. |
| `11-binary_to_decimal` | Convertit la valeur binaire de `BINARY` en décimal. |
| `12-combinations` | Affiche toutes les combinaisons de deux lettres minuscules, sauf `oo`. |
| `13-print_float` | Affiche `NUM` avec exactement deux chiffres après la virgule. |

> **Attention :** l'exercice `0-alias` définit un alias destructeur. Il doit uniquement être testé dans un environnement temporaire, sans fichiers importants.

## 💻 Exemples pratiques

### Exemple 1 — Créer une variable locale

**Script :** `6-create_local_variable`

```bash
#!/bin/bash
BEST="School"
```

Ce script crée une variable Shell nommée `BEST`.

### Exemple 2 — Créer une variable d'environnement

**Script :** `7-create_global_variable`

```bash
#!/bin/bash
export BEST="School"
```

La commande `export` permet de transmettre cette variable aux processus enfants du Shell qui l'exécute.

### Exemple 3 — Compter les entrées de PATH

**Script :** `3-paths`

```bash
#!/bin/bash
printf '%s\n' "$PATH" | tr ':' '\n' | wc -l
```

Ce script compte les entrées séparées par des deux-points dans la variable `PATH`.

### Exemple 4 — Effectuer une opération arithmétique

**Script :** `9-divide_and_rule`

```bash
#!/bin/bash
echo $((POWER / DIVIDE))
```

L'expansion arithmétique Bash permet d'effectuer une division entière. La variable `DIVIDE` ne doit pas être égale à zéro.

### Exemple 5 — Convertir un nombre binaire en décimal

**Script :** `11-binary_to_decimal`

```bash
#!/bin/bash
echo $((2#$BINARY))
```

Le préfixe `2#` indique à Bash que la valeur doit être interprétée en base 2.

## ⚙️ Prérequis techniques

| Exigence | Spécification |
|---|---|
| Système d'exploitation | Ubuntu 20.04 LTS |
| Interpréteur | Bash |
| Shebang | `#!/bin/bash` |
| Format des fichiers | Fins de ligne Unix |
| Exécution | `chmod u+x` |
| Dépendances | Utilitaires Unix standards et commandes internes Bash |

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
cd holbertonschool-shell/init_files_variables_and_expansions
```

### 3. Rendre un script exécutable

```bash
chmod u+x 7-create_global_variable
```

### 4. Exécuter le script

```bash
./7-create_global_variable
```

### 5. Tester la création d'une variable

Pour modifier les variables de la session Shell courante, utilise `source` :

```bash
source ./7-create_global_variable
echo "$BEST"
```

Résultat attendu :

```text
School
```

**Important :** lorsqu'un script est exécuté avec `./script`, il démarre un processus Bash séparé. Les variables définies dans ce processus ne sont pas conservées dans le Shell parent. La commande `source` permet d'exécuter le script directement dans la session courante.

## 🧠 Compétences développées

Ce projet permet d'approfondir les connaissances suivantes :

- Initialisation et configuration de Bash.
- Variables locales et variables d'environnement.
- Transmission des variables aux processus enfants.
- Configuration de PATH et recherche des exécutables.
- Expansions de paramètres, arithmétiques et d'accolades.
- Alias et personnalisation du terminal.
- Calculs entiers et conversions entre bases numériques.
- Programmation Bash et automatisation.

---

**Dépôt :** `holbertonschool-shell`  
**Répertoire :** `init_files_variables_and_expansions`  
**Projet :** Shell — Fichiers d'initialisation, variables et expansions
