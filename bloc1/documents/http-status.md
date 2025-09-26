# 📊 Codes de statut HTTP

Les **codes de statut HTTP** sont envoyés par le serveur dans la réponse pour indiquer le **résultat d'une requête**. Chaque code est un **nombre à 3 chiffres**, classé en catégories selon sa première valeur.

---

## 📁 Catégories de codes

| Catégorie | Signification                       | Exemple       |
|-----------|-------------------------------------|---------------|
| 1xx       | 🟦 Informationnel                    | `100 Continue` |
| 2xx       | ✅ Succès                            | `200 OK`       |
| 3xx       | 🔁 Redirection                       | `301 Moved Permanently` |
| 4xx       | ⚠️ Erreur côté client                | `404 Not Found` |
| 5xx       | ❌ Erreur côté serveur               | `500 Internal Server Error` |

---

## ✅ Codes 2xx – Succès

| Code | Nom                   | Description                                  |
|------|------------------------|----------------------------------------------|
| 200  | OK                     | La requête a réussi.                         |
| 201  | Created                | Une ressource a été créée.                   |
| 204  | No Content             | Requête réussie, mais aucune réponse à renvoyer. |

---

## 🔁 Codes 3xx – Redirection

| Code | Nom                   | Description                                  |
|------|------------------------|----------------------------------------------|
| 301  | Moved Permanently      | La ressource a été déplacée définitivement.  |
| 302  | Found (Moved Temporarily) | Redirection temporaire.                |
| 304  | Not Modified           | La ressource n’a pas changé (utilisé avec cache). |

---

## ⚠️ Codes 4xx – Erreurs client

| Code | Nom                   | Description                                  |
|------|------------------------|----------------------------------------------|
| 400  | Bad Request            | Syntaxe de requête invalide.                 |
| 401  | Unauthorized           | Authentification requise.                    |
| 403  | Forbidden              | Accès refusé, même avec authentification.    |
| 404  | Not Found              | Ressource non trouvée.                       |
| 405  | Method Not Allowed     | Méthode HTTP non autorisée pour cette ressource. |

---

## ❌ Codes 5xx – Erreurs serveur

| Code | Nom                   | Description                                  |
|------|------------------------|----------------------------------------------|
| 500  | Internal Server Error  | Erreur générique du serveur.                |
| 502  | Bad Gateway            | Le serveur agit en tant que proxy/gateway et reçoit une mauvaise réponse. |
| 503  | Service Unavailable    | Serveur temporairement indisponible.         |

---

## 🛠️ Exemple avec `curl`

```bash
curl -i https://exemple.com/ressource-inexistante
Réponse :

http
Copier le code
HTTP/1.1 404 Not Found
Content-Type: text/html; charset=UTF-8
🔎 À savoir
Les codes 2xx ne signifient pas toujours que tout s'est bien passé côté applicatif, seulement que la requête HTTP est correcte.

Un 404 n’est pas forcément une erreur grave, juste une information que la ressource est absente.

Les APIs REST utilisent souvent 201 Created pour la création de ressource.

🧠 Les codes de statut sont essentiels pour diagnostiquer les problèmes, automatiser les comportements, ou interagir proprement avec une API.

less
Copier le code
