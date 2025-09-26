# 🔗 Structure d’une URL (Uniform Resource Locator)

Une **URL** est une adresse qui permet de localiser une ressource sur le web. Elle suit une syntaxe standardisée composée de plusieurs parties.

---

## 📐 Syntaxe générale

schéma://utilisateur:motdepasse@hôte:port/chemin?query#fragment

yaml
Copier le code

---

## 🔍 Explications des composants

| Partie           | Description                                                      | Exemple                 |
|------------------|-----------------------------------------------------------------|-------------------------|
| `schéma`         | Protocole utilisé (http, https, ftp, mailto, etc.)              | `https`                 |
| `utilisateur:motdepasse` | Optionnel, informations d’authentification               | `user:pwd`              |
| `hôte`           | Nom de domaine ou adresse IP du serveur                         | `www.exemple.com`       |
| `port`           | Numéro de port (optionnel, défaut 80 pour HTTP, 443 pour HTTPS) | `8080`                  |
| `chemin`         | Chemin vers la ressource sur le serveur                         | `/dossier/page.html`    |
| `query`          | Paramètres passés à la ressource, sous forme clé=valeur         | `id=123&type=pdf`       |
| `fragment`       | Ancre ou section spécifique dans la page                        | `section2`              |

---

## 📚 Exemple complet

https://user:password@www.exemple.com:8080/dossier/page.html?id=123&type=pdf#section2

markdown
Copier le code

- **Protocole** : `https`  
- **Utilisateur/Mot de passe** : `user:password`  
- **Hôte** : `www.exemple.com`  
- **Port** : `8080`  
- **Chemin** : `/dossier/page.html`  
- **Paramètres** : `id=123&type=pdf`  
- **Fragment** : `section2`

---

## 🛠️ Notes pratiques

- Le port est souvent omis si c’est le port standard (80 pour HTTP, 443 pour HTTPS).  
- Les paramètres dans la partie `query` sont séparés par `&` et encodés en URL (ex : espaces remplacés par `%20`).  
- Le fragment n’est jamais envoyé au serveur, il sert uniquement à la navigation côté client.

---

## 🔧 Exemple d’URL simplifiée

https://www.exemple.com/articles?page=2#comments

yaml
Copier le code

- Accède à la page des articles.  
- Affiche la page 2 (paramètre `page=2`).  
- Va directement à la section des commentaires (`#comments`).

---

> 💡 Comprendre la structure d’une URL est essentiel pour manipuler les liens, les requêtes HTTP, et les paramètres dans les applications web.