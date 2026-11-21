# Aide-mémoire du terminal Linux

## Se déplacer

| Commande    | Ce qu'elle fait                   | Exemple     |
| ----------  | --------------------------------- | ----------- |
| `pwd`       | Affiche le dossier où je suis     | `pwd`       |
| `cd`        | Change de dossier                 | `cd ~/dev`  |
| `cd ..`     | Remonte d'un niveau               | `cd ..`     |
| `cd ~`      | Revient au dossier personnel      | `cd ~`      |
| `ls`        | Affiche le contenu du dossier     | `ls`        |
| `ls -l`     | Affiche le contenu en détail      | `ls -l`     |
| `ls -a`     | Affiche aussi les fichiers cachés | `ls -a`     |
| `clear`     | Efface l'écran                    | `clear`     |
| `whoami`    | Affiche mon nom d'utilisateur     | `whoami`    |
| `ls --help` | Affiche l'aide de la commande ls  | `ls --help` |

## Fichiers et dossiers

| Commande   | Ce qu'elle fait                    | Exemple                         |
| ---------- | ---------------------------------- | ------------------------------- |
| `mkdir`    | Crée un dossier                    | `mkdir photos`                  |
| `mkdir -p` | Crée plusieurs niveaux de dossiers | `mkdir -p projet/assets/images` |
| `touch`    | Crée un fichier vide               | `touch vide.txt`                |
| `cp`       | Copie un fichier                   | `cp a.txt b.txt`                |
| `cp -r`    | Copie un dossier et son contenu    | `cp -r projet sauvegarde`       |
| `mv`       | Déplace ou renomme un fichier      | `mv notes.txt idees.txt`        |
| `rm`       | Supprime un fichier                | `rm notes.txt`                  |
| `rm -i`    | Supprime après confirmation        | `rm -i notes.txt`               |
| `rmdir`    | Supprime un dossier vide           | `rmdir photos`                  |
| `rm -r`    | Supprime un dossier et son contenu | `rm -r photos`                  |

## Lire et chercher

| Commande     | Ce qu'elle fait                               | Exemple                 |
| ------------ | --------------------------------------------- | ----------------------- |
| `cat`        | Affiche tout le fichier                       | `cat notes.txt`         |
| `less`       | Affiche le fichier page par page              | `less notes.txt`        |
| `head -n 5`  | Affiche les 5 premières lignes                | `head -n 5 notes.txt`   |
| `tail -n 5`  | Affiche les 5 dernières lignes                | `tail -n 5 notes.txt`   |
| `wc -l`      | Compte les lignes                             | `wc -l notes.txt`       |
| `grep`       | Affiche les lignes qui contiennent un mot     | `grep ERROR app.log`    |
| `grep -i`    | Cherche sans tenir compte des majuscules      | `grep -i error app.log` |
| `grep -c`    | Compte les lignes qui contiennent le mot      | `grep -c ERROR app.log` |
| `grep -r`    | Cherche dans tous les fichiers du dossier     | `grep -r "todo" .`      |
| `grep -r -l` | Affiche seulement le nom des fichiers trouvés | `grep -r -l "todo" .`   |
| `find`       | Retrouve un fichier par son nom               |  `find . -name "*.js"`  |
## Scripts

| Commande      | Ce qu'elle fait                                      | Exemple                        |
| ------------- | ---------------------------------------------------- | ------------------------------ |
| `#!/bin/bash` | Première ligne d'un script : indique d'utiliser bash | `#!/bin/bash`                  |
| `chmod +x`    | Donne le droit d'exécution à un fichier              | `chmod +x scripts/verifier.sh` |
| `./ `         | Lance un script du dossier courant                   | `./scripts/verifier.sh`        |

## Versions

| Commande         | Ce qu'elle fait                      | Exemple          |
| ---------------- | ------------------------------------ | ---------------- |
| `--version`      | Affiche la version d'un outil        | `node --version` |
| `lsb_release -d` | Affiche la version d'Ubuntu          | `lsb_release -d` |
| `which`          | Indique où un programme est installé | `which node`     |


## Branches

- `git branch` : afficher les branches locales.
- `git branch -a` : afficher les branches locales et distantes.
- `git switch nom-branche` : changer de branche.
- `git switch -c nom-branche` : créer une branche.
- `git merge nom-branche` : fusionner une branche.
- `git branch -d nom-branche` : supprimer une branche fusionnée.
- `git log --oneline --graph --all` : afficher l'historique des branches.
