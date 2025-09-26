# Méthodes HTTP : GET et POST
## Qu’est-ce que la méthode GET ?

La méthode GET est utilisée pour **demander** des informations au serveur.  
Les données sont envoyées dans l’URL, sous forme de paramètres.  
Elle ne modifie pas les données sur le serveur.

## Qu’est-ce que la méthode POST ?

La méthode POST est utilisée pour **envoyer** des données au serveur, par exemple un formulaire ou un fichier.  
Les données sont envoyées dans le **corps** de la requête HTTP.  
Cette méthode peut modifier les données sur le serveur.
## Exemple de requête GET

URL : `http://dev.local/api/users?q=alice`

Requête :

GET /api/users?q=alice HTTP/1.1
Host: dev.local
Accept: application/json

vbnet
Copier le code

Pas de corps dans une requête GET.

Réponse :

HTTP/1.1 200 OK
Content-Type: application/json

[
{"id":1, "name":"Alice"}
]
HTTP/1.1 201 Created
Content-Type: application/json

{
"id": 2,
"name": "Bob"
}
## Comparaison entre GET et POST

| Critère            | GET                       | POST                      |
|--------------------|---------------------------|---------------------------|
| Données visibles   | Oui, dans l’URL            | Non, dans le corps         |
| Idempotence        | Oui                       | Non                       |
| Mise en cache      | Oui                       | Généralement non           |
| Taille des données | Limitée (URL max ~2000)   | Plus grande                |
| Usage typique      | Lire ou chercher des données | Envoyer ou créer des données |
## Résumé

- GET est utilisé pour **lire** des données, sans modifier le serveur.  
- POST est utilisé pour **envoyer** des données, souvent pour créer ou modifier.  
- GET transmet les données dans l’URL, POST dans le corps.  
- POST est plus sécurisé car les données ne sont pas visibles dans l’URL.