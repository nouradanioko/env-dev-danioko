# Journal des choix

## 2026-11-10 – Système pour le terminal

- **Décision :** utiliser Ubuntu dans WSL sur mon ordinateur Windows.
- **Autres possibilités :** une machine virtuelle classique, un double démarrage Windows et Linux.
- **Raison :** WSL est rapide à installer, ne demande pas de tout redémarrer à chaque fois, et donne les mêmes commandes que sur les serveurs.

## 2026-11-10 – Éditeur de code

- **Décision :** utiliser VS Code.
- **Autres possibilités :** nano dans le terminal, un autre éditeur.
- **Raison :** VS Code était déjà installé, il ouvre les dossiers d'Ubuntu, a un terminal intégré et affiche le rendu des fichiers Markdown.

## 2026-11-12 – Installation de Node.js

- **Décision :** installer Node.js avec le dépôt NodeSource et apt.
- **Autres possibilités :** le paquet nodejs d'Ubuntu, le site nodejs.org.
- **Raison :** NodeSource donne la version LTS récente, et les commandes peuvent être écrites dans mon README pour être refaites à l'identique.

## 2026-11-12 – Version de Node.js : LTS

- **Décision :** utiliser une version LTS de Node.js (numéro majeur pair).
- **Autres possibilités :** une version impaire plus récente.
- **Raison :** une version LTS est maintenue longtemps et reste plus stable ; toute personne qui refait mon installation obtient la même.

## 2026-11-15 – Scripts d'installation et de vérification

- **Décision :** écrire les scripts installer.sh et verifier.sh.
- **Autres possibilités :** expliquer chaque commande par écrit seulement, installer les outils à la main.
- **Raison :** un script n'oublie aucune étape, va plus vite, et n'importe qui peut le lancer. C'est un pas de plus vers la reproductibilité.