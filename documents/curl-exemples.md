# 🚀 Exemples pratiques avec `curl`

`curl` est un outil en ligne de commande très puissant pour envoyer des requêtes HTTP et tester des API ou sites web.

---

## 1. Faire une requête GET simple

```bash
curl https://exemple.com
Cette commande récupère le contenu de la page à l’URL indiquée.

2. Voir les en-têtes de la réponse
bash
Copier le code
curl -I https://exemple.com
Le paramètre -I (ou --head) demande uniquement les en-têtes HTTP.

3. Faire une requête POST avec des données
bash
Copier le code
curl -X POST -d "nom=Jean&age=30" https://exemple.com/api/utilisateur
-X POST : spécifie la méthode POST.

-d : données envoyées au serveur (formulaire URL-encodé par défaut).

4. Envoyer des données JSON avec POST
bash
Copier le code
curl -X POST -H "Content-Type: application/json" \
     -d '{"nom": "Jean", "age": 30}' \
     https://exemple.com/api/utilisateur
-H : ajoute un en-tête HTTP (Content-Type ici).

Le corps de la requête est un JSON.

5. Ajouter un en-tête personnalisé
bash
Copier le code
curl -H "Authorization: Bearer TOKEN123" https://exemple.com/api/secret
Utilisé souvent pour l’authentification via token.

6. Télécharger un fichier
bash
Copier le code
curl -O https://exemple.com/image.png
Le paramètre -O télécharge le fichier et le sauvegarde sous son nom d’origine.

7. Suivre les redirections
bash
Copier le code
curl -L http://exemple.com
Avec -L, curl suit automatiquement les redirections HTTP (codes 3xx).

8. Spécifier le type de contenu attendu (négociation)
bash
Copier le code
curl -H "Accept: application/json" https://exemple.com/api/data
9. Afficher la requête complète (pour débogage)
bash
Copier le code
curl -v https://exemple.com
Le mode verbeux -v affiche les détails de la requête et réponse.

10. Utiliser l’authentification basique HTTP
bash
Copier le code
curl -u utilisateur:motdepasse https://exemple.com/api
💡 Astuce : vous pouvez combiner plusieurs options pour tester précisément vos requêtes HTTP.