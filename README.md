# TP 01 - HTTP : Le jeu de piste

**Nom :** Emma-Gabrielle FOUGEROUX <br>
**Classe :** BTS SIO SLAM 2

---

## Mission 0 : Découverte des outils (Postman et Bruno)

###  1. Outils utilisés
Pour ce TP, j'ai installé et testé deux clients HTTP :
* **Postman** : outil complet nécessitant un compte (connecté via GitHub).
* **Bruno** : client léger, open source et sans compte nécessaire.

---

### 2. Requête GET simple

* **URL :** `https://jsonplaceholder.typicode.com/posts`
* **Méthode :** `GET`
* **Objectif :** Récupérer la liste des articles.
* **Code retour obtenu :** `200 OK` (requête réussie).
* **Réponse :** Tableau JSON contenant la liste des articles.

#### Captures d'écran GET :

#### Postman
![GET Postman](postman_get.png)
![POST Postman](postman_post.png)

#### Bruno
![GET Bruno](bruno_get.png)
![POST Bruno](bruno_post.png)

---

### 3. Requête POST avec données

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
```

---

## Mission 1 : Le jeu de piste HTTP (9 étapes)

L'objectif de cette mission est de résoudre les énigmes successives en manipulant différentes méthodes HTTP (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`), des paramètres d'URL, des en-têtes personnalisés et des corps de requête (Body).

* **Serveur cible :** `http://172.16.3.254:8001`
* **Collection Postman associée :** `TP1-Mission_1.postman_collection.json`

---

### Étape 1 : Bienvenue
* **Méthode :** `GET`
* **URL :** `http://172.16.3.254:8001/bienvenue`
* **Description :** Premier point d'entrée du jeu de piste.

---

### Étape 2 : Découverte des paramètres
* **Méthode :** `GET`
* **URL :** `http://172.16.3.254:8001/decouverte-des-parametres?nom=Emma-Gabrielle`
* **Paramètres de requête (Query Params) :**
  * `nom` : `Emma-Gabrielle`

---

### Étape 3 : Plusieurs paramètres
* **Méthode :** `GET`
* **URL :** `http://172.16.3.254:8001/plusieurs-parametres?prenom=Emma-Gabrielle&age=20`
* **Paramètres de requête (Query Params) :**
  * `prenom` : `Emma-Gabrielle`
  * `age` : `20`

---

### Étape 4 : Un peu de POST
* **Méthode :** `POST`
* **URL :** `http://172.16.3.254:8001/un-peu-de-post`
* **Description :** Passage à la méthode `POST` pour interagir avec le serveur.

---

### Étape 5 : Content-Type et Body JSON
* **Méthode :** `POST`
* **URL :** `http://172.16.3.254:8001/5-content-type`
* **En-tête (Header) :**
  * `Content-Type: application/json`
* **Corps envoyé (Body raw JSON) :**
```json
{
  "message": "test"
}
```

---

### Étape 6 : Méthode PUT et négociation de contenu
* **Méthode :** `PUT`
* **URL :** `http://172.16.3.254:8001/put-method-6`
* **En-têtes (Headers) :**
  * `Content-Type: text/html`
  * `Accept: application/json`
* **Corps envoyé (Body raw Text/HTML) :**
```html
<p>Mise à jour</p>
```

---

### Étape 7 : Méthode DELETE avec paramètre
* **Méthode :** `DELETE`
* **URL :** `http://172.16.3.254:8001/et-oui-delete?filename=test.txt`
* **Paramètres de requête (Query Params) :**
  * `filename` : `test.txt`

---

### Étape 8 : Méthode PATCH et mise à jour partielle
* **Méthode :** `PATCH`
* **URL :** `http://172.16.3.254:8001/etape8/api/users/12345`
* **En-tête (Header) :**
  * `Content-Type: application/json`
* **Corps envoyé (Body raw JSON) :**
```json
{
  "role": "Developer",
  "email": "emma@test.fr"
}
```

---

### Étape 9 : Authentification, User-Agent et validation finale
* **Méthode :** `POST`
* **URL :** `http://172.16.3.254:8001/etape9`
* **En-têtes (Headers) :**
  * `Content-Type: application/json`
  * `api-key: FenelonBTSSIO`
  * `User-Agent: FenelonBTSSIO-UserAgent-LaRochelle-v1.0`
* **Corps envoyé (Body raw JSON) :**
```json
{
  "name": "Donald Duck"
}
```












