# TP 01 - HTTP : Le jeu de piste
**Mission 0 : Découverte des outils (Postman et Bruno)**

**Nom :** Emma-Gabrielle FOUGEROUX <br>
**Classe :** BTS SIO SLAM 2

---

## 1. Outils utilisés
Pour ce TP, j'ai installé et testé deux clients HTTP :
* **Postman** : outil complet nécessitant un compte (connecté via GitHub).
* **Bruno** : client léger, open source et sans compte nécessaire.

---

## 2. Requête GET simple

* **URL :** `https://jsonplaceholder.typicode.com/posts`
* **Méthode :** `GET`
* **Objectif :** Récupérer la liste des articles.
* **Code retour obtenu :** `200 OK` (requête réussie).
* **Réponse :** Tableau JSON contenant la liste des articles.

### Captures d'écran GET :

#### Postman
![GET Postman](screenshots/postman_get.png)
![POST Postman](screenshots/postman_post.png)

#### Bruno
![GET Bruno](screenshots/bruno_get.png)
![POST Bruno](screenshots/bruno_post.png)

---

## 3. Requête POST avec données

* **URL :** `https://jsonplaceholder.typicode.com/posts`
* **Méthode :** `POST`
* **Header ajouté :** `Content-Type: application/json`
* **Corps envoyé (Body JSON) :**
```json
{
  "title": "Mon premier post",
  "body": "Créé avec Postman / Bruno",
  "userId": 1
}
