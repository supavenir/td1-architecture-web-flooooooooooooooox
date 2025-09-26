# 🌍 Négociation de contenu HTTP

La **négociation de contenu** (en anglais *Content Negotiation*) est un mécanisme du protocole HTTP qui permet au **client** et au **serveur** de s’accorder sur le **format de la réponse**.

Elle permet, par exemple, qu’un même URL puisse renvoyer soit du **HTML**, soit du **JSON**, soit un autre type de contenu, selon ce que préfère le client (navigateur, API, etc.).

---

## 🔄 Principe de fonctionnement

Le client peut envoyer dans la requête HTTP des **en-têtes spéciaux** pour indiquer :

- Le type de contenu qu’il accepte (`Accept`)
- La langue préférée (`Accept-Language`)
- L’encodage souhaité (`Accept-Encoding`)
- Le charset (`Accept-Charset`)

Le serveur analyse ces en-têtes et répond avec le contenu le plus adapté, s’il est disponible.

---

## 📥 Exemple de requête HTTP

```http
GET /data HTTP/1.1
Host: exemple.com
Accept: application/json
Accept-Language: fr
📤 Exemple de réponse du serveur
http
Copier le code
HTTP/1.1 200 OK
Content-Type: application/json
Content-Language: fr

{
  "message": "Bonjour le monde"
}
📌 Principaux en-têtes de négociation
En-tête	Description
Accept	Types MIME que le client accepte (text/html, application/json, etc.)
Accept-Language	Langues préférées (fr, en-US, etc.)
Accept-Encoding	Méthodes de compression acceptées (gzip, deflate, etc.)
Accept-Charset	Jeux de caractères (utf-8, etc.)

✅ Avantages
Permet une flexibilité côté client.

Favorise la réutilisation d’URL unique pour plusieurs formats.

Utile pour les APIs RESTful, qui peuvent renvoyer JSON ou XML selon le client.

⚠️ Remarques
Tous les serveurs ne prennent pas en charge la négociation de contenu.

Parfois, on utilise plutôt des extensions d’URL (/data.json, /data.xml) ou des paramètres de requête (?format=json).

🛠️ Test avec curl
Voici comment tester la négociation de contenu avec curl :

bash
Copier le code
curl -H "Accept: application/json" https://api.exemple.com/data