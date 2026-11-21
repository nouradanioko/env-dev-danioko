# env-dev-danioko – Mon environnement de développement (B1 DEV, IFRAN)
 
Environnement de développement de Danioko Rafiatou Noura – B1 DEV, IFRAN. 
 
## Mon ordinateur 
 
| Élément     | Valeur                    | 
| ----------- | -------------------       | 
| Système     | Windows 11 Professionnel  | 
| Processeur  | Intel Core i7             | 
| Mémoire     | 16 Go                     | 
| Éditeur     | VS Code                   | 
 
## Mon Ubuntu 
 
| Élément      | Valeur               | 
| ------------ | -------------------- | 
| Version      | Ubuntu 26.04.1 LTS   | 
| Lancé avec   | WSL                  | 
| Processeurs  | 8                    | 
| Mémoire      | 7,6 Go               | 
| Utilisateur  | zbook                | 

## Logiciels installés dans Ubuntu

| Logiciel| Version | Commande d'installation                           |
| ------- | ------- | -----------------------------                     |
| Git     | 2.53.0  | déjà présent dans Ubuntu                          |
| tree    | 2.3.1   | sudo apt install -y tree                          |
| htop    | 3.4.1   | sudo apt install -y htop                          |
| nano    | 8.7.1   | sudo apt install -y nano                          |
| Node.js | 26.13.1 | dépôt NodeSource, puis sudo apt install -y nodejs |
| npm     | 11.20.0 | installé avec Node.js                             |

## Contenu du dossier

| Dossier / Fichier         | Description                               |
|---------------------------|-------------------------------------------|
| `docs/`                   | Documents du projet                       |
| `docs/aide-memoire.md`    | Fiche aide-mémoire                        |
| `docs/reseau.md`          | Fiche réseau : adresses IP et DNS         |
| `scripts/`                | Scripts du projet                         |
| `scripts/installer.sh`    | Script d'installation des outils          |
| `scripts/verifier.sh`     | Script de vérification de l'environnement |
| `JOURNAL.md`              | Journal de suivi du projet                |
| `.gitignore`               | Fichiers que Git ne suit pas              |
| `README.md`               | Présentation et documentation du projet   |

## Installation

### 1. Installer Ubuntu et VS Code

- **Windows :** dans le Terminal (administrateur), taper `wsl --install`,
  redémarrer, puis choisir un nom d'utilisateur et un mot de passe Ubuntu.
- **Mac :** installer Homebrew depuis [brew.sh](https://brew.sh), puis taper
  `brew install colima docker`, `colima start` et `colima ssh`.
- Installer VS Code depuis [code.visualstudio.com](https://code.visualstudio.com).

### 2. Installer les outils dans Ubuntu

1. Ouvrir Ubuntu et copier le projet : `git clone https://github.com/nouradanioko/env-dev-danioko.git ~/dev/env-dev-danioko`
2. Aller dans le dossier du projet : `cd ~/dev/env-dev-danioko`
3. Lancer le script d'installation : `./scripts/installer.sh`

## Vérification

Lancer `./scripts/verifier.sh` dans Ubuntu.
Résultat attendu : une version pour Ubuntu, Git, Node.js, npm et tree.
