# 📋 En-têtes HTTP (HTTP Headers)

Les **en-têtes HTTP** sont des paires clé-valeur envoyées dans les requêtes et réponses HTTP. Ils permettent de transmettre des informations supplémentaires sur la requête ou la réponse.

---

## 1. En-têtes courants dans la requête HTTP

| En-tête           | Description                                               | Exemple                                  |
|-------------------|-----------------------------------------------------------|------------------------------------------|
| `Host`            | Nom du serveur et port (obligatoire HTTP/1.1)            | `Host: exemple.com`                      |
| `User-Agent`      | Informations sur le client (navigateur, outil, etc.)      | `User-Agent: Mozilla/5.0`                |
| `Accept`          | Types MIME que le client accepte                           | `Accept: text/html,application/json`    |
| `Accept-Language` | Langues préférées                                         | `Accept-Language: fr-FR,fr;q=0.9,en;q=0.8` |
| `Accept-Encoding` | Types de compression acceptés                              | `Accept-Encoding: gzip, deflate`        |
| `Authorization`   | Informations d’authentification                            | `Authorization: Bearer TOKEN123`         |
| `Cookie`          | Données de cookie envoyées au serveur                      | `Cookie: sessionId=abc123`               |
| `Content-Type`    | Type MIME du corps de la requête (pour POST, PUT, etc.)   | `Content-Type: application/json`         |

---

## 2. En-têtes courants dans la réponse HTTP

| En-tête           | Description                                               | Exemple                                  |
|-------------------|-----------------------------------------------------------|------------------------------------------|
| `Content-Type`    | Type MIME du corps de la réponse                           | `Content-Type: text/html; charset=UTF-8` |
| `Content-Length`  | Taille du corps en octets                                  | `Content-Length: 348`                    |
| `Set-Cookie`      | Envoie un cookie au client                                | `Set-Cookie: sessionId=abc123; HttpOnly` |
| `Cache-Control`   | Directives de mise en cache                               | `Cache-Control: no-cache, no-store`     |
| `Location`        | URL de redirection                                        | `Location: https://exemple.com/nouvelle-page` |
| `Expires`         | Date d’expiration du contenu                              | `Expires: Wed, 21 Oct 2025 07:28:00 GMT` |
| `ETag`            | Identifiant de version de la ressource                    | `ETag: "abc123xyz"`                     |
| `WWW-Authenticate`| Challenge d’authentification (lorsqu’une auth est requise)| `WWW-Authenticate: Basic realm="Exemple"` |

---

## 3. Exemples de requête et réponse avec en-têtes

### Requête HTTP

```http
GET /page HTTP/1.1
Host: exemple.com
User-Agent: Mozilla/5.0 (Windows NT 10.0)
Accept: text/html,application/xhtml+xml
Accept-Language: fr-FR,fr;q=0.9,en-US;q=0.8,en;q=0.7
Réponse HTTP
http
Copier le code
HTTP/1.1 200 OK
Content-Type: text/html; charset=UTF-8
Content-Length: 1024
Cache-Control: max-age=3600
Set-Cookie: sessionId=abc123; HttpOnly; Secure
4. Pourquoi les en-têtes sont importants ?
Contrôle du contenu : format, encodage, langue.

Gestion des sessions : via cookies ou tokens.

Sécurité : authentification, directives de cache.

Performance : contrôle de la mise en cache.

5. Tester les en-têtes avec curl
bash
Copier le code
curl -I https://exemple.com
Cette commande affiche uniquement les en-têtes de la réponse.

📌 Les en-têtes HTTP sont essentiels pour comprendre et maîtriser les échanges entre client et serveur.

css
Copier le code

Veux-tu que je t’aide à ajouter une section sur les en-têtes spécifiques à la sécurité (CORS, CSP, HSTS, etc.) ?