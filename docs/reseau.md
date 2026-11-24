# Fiche réseau

## Mes adresses IP

| Machine                | Adresse IP | Privée ou publique ? |
| ---------------------- | ---------- | -------------------- |
| Mon Ubuntu             | 172.24.137.47 | Privée |
| Mon ordinateur (Wi-Fi) | 172.16.51.19 | Privée |
| Ma connexion Internet  | (non publiée) | publique |

## Résultats du DNS

| Nom de domaine  | Adresse IP     
| --------------- | ----------    |
| `github.com`    | 140.82.121.3  |
| `wikipedia.org` | 185.15.59.224 |

## Les outils réseau

| Commande          | Ce qu'elle fait |
| ----------------- | --------------- |
| `hostname -I`     | Affiche l'adresse IP de mon Ubuntu |
| `ping -c 4 <nom>` | Vérifie la connexion avec un ordinateur ou un serveur |
| `nslookup <nom>`  | Recherche l'adresse IP associée à un nom de domaine |

## Le trajet d'une requête 
 
Quand je tape `https://github.com` dans mon navigateur : 

1. Le navigateur identifie le nom de domaine `github.com`.
2. Le DNS recherche l'adresse IP correspondante.
3. Le DNS renvoie l'adresse IP du serveur.
4. Le navigateur se connecte au serveur.
5. Le navigateur envoie une requête HTTP pour demander la page.
6. Le serveur renvoie une réponse et le navigateur affiche la page Web.
 
## Les codes de réponse HTTP

| Code | Nom                   | Ce qu'il veut dire | Exemple que j'ai vu |
| ---- | --------------------- | ------------------ | ------------------- |
| 200  | OK                    | La demande a réussi. Le serveur a renvoyé la page demandée. | Une page Web s'affiche correctement. |
| 301  | Moved Permanently     | La page a été déplacée définitivement vers une nouvelle adresse. | Redirection vers une nouvelle URL. |
| 404  | Not Found             | La page demandée est introuvable sur le serveur. | Une page affiche « 404 Not Found ». |
| 500  | Internal Server Error | Le serveur rencontre un problème interne. | (pas vu) |

## Les ports

| Port | Service | Exemple d'URL |
| ---- | ------- | ------------- |
| 80 | HTTP | http://exemple.com |
| 443 | HTTPS | https://github.com |
| 8000 | Serveur de développement | http://localhost:8000 |

## Diagnostiquer une erreur

Les 4 questions, dans l'ordre :

1. Le nom est-il trouvé ? → `nslookup <nom>`
2. La machine répond-elle ? → `ping -c 4 <nom>`
3. Un serveur écoute-t-il le port ? → `curl -I <url>` ou `ss -tln`
4. Que répond le serveur ? → code de réponse et journal du serveur

### Exemple : une panne que j'ai réparée

- **Symptôme :** la page À propos affiche une erreur 404
- **Étape :** 6, la réponse
- **Cause :** le lien demande a-propos.html mais le fichier s'appelle apropos.html
- **Correction :** `mv apropos.html a-propos.html`
- **Vérification :** la page s'affiche et le journal montre 200