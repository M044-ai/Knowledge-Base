Bon la longueur du plan d'apprentissage mettait vraiment le bazar dans la conv sur un sujet trop spécifique, j'ai tout migré dans le fil 
# 🧭 __**SOMMAIRE**__


## 🧑‍🏫 **Plan de formation**

* 🔽 Introduction
* 1️⃣ Comprendre JavaScript moderne

* 2️⃣ TypeScript
* 3️⃣ Node.js et API

* 4️⃣ PostgreSQL
* 5️⃣ AWS

* 6️⃣ Relier tout
* 7️⃣ Mini projet
* 🔼 Outro :
-- 🧐 Ce que veut dire “vibe coding structuré”
-- 📢 Ce qui vous rend crédible en entretien



## 🛠️ **Quelques outils**

* 1️⃣ La stack expliquée en une page (vision simple)
* 2️⃣ Les 12 notions exactes à maîtriser pour un entretien

* 3️⃣ Mini-projet réalisable en 90 minutes
* 🔼 Outro :
-- 📢 Comment présenter ça en entretien
-- ☝️ Point important pour la promo



## 📦 **Kit de préparation d'entretien**

* 1️⃣ Définitions principales
-- TypeScript
-- API REST
-- JSON
-- PostgreSQL
-- AWS

* 2️⃣ Les 20 questions techniques probables
-- JavaScript / TypeScript
-- Backend / API
-- Base de données
-- Cloud

* ➡️ Réponses
-- JavaScript / TypeScript
-- Backend / API

-- Base de données
-- Cloud

* 3️⃣ Les 10 erreurs classiques des candidats débutants

* 4️⃣ Conseils stratégiques pour votre promo
--  Le message de l’employeur
-- Pour des profils non-dev
-- La clé de l'entretien


# 🧑‍🏫 Plan de formation :

---

Voici le **plan d’apprentissage 7 jours**, repris tel quel dans son principe, mais enrichi avec **du matériel pédagogique rapide (YouTube + pages d’introduction)** adapté à quelqu’un qui part de zéro et doit **comprendre vite plutôt que maîtriser**.

Les ressources sont majoritairement **courtes, pédagogiques et orientées compréhension**, pas formation longue.

---

## 🔽  Introduction : Vision globale de la stack demandée

L’employeur décrit en fait une architecture très classique :

```
Frontend (web)
        ↓
API Node.js / TypeScript
        ↓
PostgreSQL (base de données)
        ↓
AWS (hébergement et infrastructure)
```

🎯  __Votre objectif__ : **comprendre ce pipeline**.

---

## 1️⃣ Comprendre JavaScript moderne

Base indispensable pour comprendre TypeScript.

À voir :

* variables
* fonctions
* objets
* async / await
* modules

###   📽️ Vidéos

* **JavaScript en 100 secondes** (très bon aperçu rapide) : [ici](https://www.youtube.com/watch?v=DHjqpvDnNGE)

* **JavaScript pour débutants – Grafikart (FR)** : [ici](https://www.youtube.com/watch?v=ItYyeQj0wIM)

### 🗒️ Lecture rapide

* MDN introduction JavaScript : [ici](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Introduction)

🎯  __Objectif__ :

> Comprendre un fichier JS sans être perdu.

---

## 2️⃣ TypeScript

Concept clé : **le typage**

À comprendre :
```
type User = {
  id: number
  name: string
}
```

Pourquoi c’est important :

* éviter les erreurs
* documenter les structures de données

À voir :

* types
* interfaces
* classes
* compilation

### 📽️ Vidéos

* **TypeScript en 100 secondes** : [ici](https://www.youtube.com/watch?v=zQnBQ4tB3ZA)

* **Introduction TypeScript (FR)** : [ici](https://www.youtube.com/watch?v=X8F0hU7FJx4)

### 🗒️ Lecture

Documentation officielle : [ici](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)

🎯  __Objectif__ :

> lire du TypeScript et comprendre les types.

---

## 3️⃣ Node.js et API

Ici vous comprenez **comment une application parle avec une base de données**.

Concept :

```
client → API → base de données
```

À apprendre :

* API REST
* endpoints
* JSON

Exemple :
```
GET /users
POST /orders
```

### 📽️ Vidéos

* **REST API expliquée simplement** : [ici](https://www.youtube.com/watch?v=-MTSQjw5DrM)

* **Node.js expliqué en 100 secondes** : [ici](https://www.youtube.com/watch?v=TlB_eWDSMt4)

### 🗒️ Lecture

Introduction REST API : [ici](https://restfulapi.net/)

🎯  __Objectif__ :

> comprendre ce que fait un backend.

```GET /users
POST /orders
```

### 📽️ Vidéos

* **REST API expliquée simplement** : [ici](https://www.youtube.com/watch?v=-MTSQjw5DrM)

* **Node.js expliqué en 100 secondes** : [ici](https://www.youtube.com/watch?v=TlB_eWDSMt4)

### 🗒️ Lecture

Introduction REST API : [ici](https://restfulapi.net/)

🎯  __Objectif__ :

> comprendre ce que fait un backend.

---

## 4️⃣ PostgreSQL

Ici vous apprenez **comment les données sont stockées**.

Concepts clés :

```
table
row
column
primary key
foreign key
```

Exemple :
```
SELECT * FROM users;
```

### 📽️ Vidéos

* **SQL en 100 secondes** : [ici](https://www.youtube.com/watch?v=zsjvFFKOm3c)

* **PostgreSQL introduction (FR)** : [ici](https://www.youtube.com/watch?v=qw--VYLpxG4)

### 🗒️ Lecture

Introduction SQL (très clair) : [ici](https://sqlbolt.com/fr/)

🎯 __Objectif__ :

> Comprendre comment une API lit et écrit dans une base.

---

## 5️⃣ AWS

🎯 __Objectif__ :

> Comprendre **où tourne l’application**.

À connaître :

* EC2 → serveur
* S3 → stockage
* RDS → base PostgreSQL
* Lambda → fonctions serverless

### 📽️  Vidéos

* **AWS expliqué simplement** : [ici](https://www.youtube.com/watch?v=mxT233EdY5c)

* **AWS en 100 secondes** : [ici](https://www.youtube.com/watch?v=H4AwR_xY-Kw)

### 🗒️ Lecture

Présentation AWS : [ici](https://aws.amazon.com/fr/what-is-aws/)

🎯 __Objectif__ :

> Comprendre le déploiement.

---

## 6️⃣ Relier tout

Comprendre la chaîne complète :
```
browser
   ↓
API TypeScript
   ↓
PostgreSQL
   ↓
AWS infrastructure
```

### 📽️ Vidéo très utile

* **Comment fonctionne une application web moderne** : [ici](https://www.youtube.com/watch?v=QX4nR7ZB5w8)

C’est **la compétence la plus importante**.

---

## 7️⃣ Mini-projet

Faites un exemple simple :

API TypeScript :
```
GET /users
POST /users
```
avec base PostgreSQL.

### Tutoriel rapide

Créer une API Node + PostgreSQL : [ici](https://www.youtube.com/watch?v=ldYcgPKEZC8)

🎯 __Objectif__ :

> Pouvoir dire en entretien :
> "J’ai monté un petit service TypeScript connecté à PostgreSQL".

---
## 🔼 Outro :

### 🧐 Ce que veut dire “vibe coding structuré”

Le message de l’employeur est révélateur.

Il cherche quelqu’un qui :

* utilise l’IA pour coder vite
* **mais comprend ce qu’il fait**

Donc :

❌ Copier/coller ChatGPT
✅ Comprendre l’architecture

---

### 📢 Ce qui vous rend crédible en entretien

Vous n’avez pas besoin de savoir coder beaucoup.

Vous devez pouvoir expliquer :

1️⃣ pourquoi TypeScript est utilisé
2️⃣ comment une API parle à PostgreSQL
3️⃣ comment AWS héberge le service
4️⃣ comment l’IA peut accélérer le développement

Si vous savez ça, vous êtes déjà **au-dessus de beaucoup d’alternants**.

---


# 🛠️ Quelques outils : 
---

## 1️⃣ La stack expliquée en une page (vision simple)

### Architecture typique demandée par l’employeur
```
Utilisateur (navigateur / application)
            │
            ▼
Frontend (interface web)
            │
            ▼
API backend (Node.js + TypeScript)
            │
            ▼
Base de données (PostgreSQL)
            │
            ▼
Infrastructure cloud (AWS)
```

### Rôle de chaque élément

👉 **Frontend**
Interface utilisée par l’utilisateur.
Technologies fréquentes : React, Vue, Angular.

👉 **Backend (API)**
Programme qui gère la logique métier.

Exemples :
```
GET /users
POST /orders
GET /products
```

Technologie :

* Node.js
* TypeScript

👉 **Base de données**

Stocke les données :
```
users
orders
products
```

Technologie : PostgreSQL.

👉 **Cloud**

L’infrastructure qui fait tourner tout ça.

Services AWS fréquents :

* EC2 → serveurs
* RDS → base PostgreSQL
* S3 → stockage
* Lambda → fonctions serverless

---

## 2️⃣ Les 12 notions exactes à maîtriser pour un entretien

Si vous comprenez ces points, vous paraîtrez crédible.

### 👉 JavaScript / TypeScript

1. Différence JavaScript / TypeScript
2. Typage (types, interfaces)
3. async / await
4. Modules

📽️  Vidéo utile : [ici](https://www.youtube.com/watch?v=zQnBQ4tB3ZA)

---

### 👉 Backend

5. Ce qu’est une API REST
6. Endpoint
7. JSON

Exemple :
```
GET /users
POST /users
```

📽️ Vidéo : [ici](https://www.youtube.com/watch?v=-MTSQjw5DrM)

---

### 👉 Base de données

8. Table
9. Relation
10. Requête SQL

Exemple :
```
SELECT * FROM users
```

Tutoriel rapide : [ici](https://sqlbolt.com/fr/)

---

### 👉 Cloud

11. Pourquoi on utilise le cloud
12. Rôle d’AWS dans une application

📽️ Vidéo : [ici](https://www.youtube.com/watch?v=mxT233EdY5c)

---


## 3️⃣ Mini-projet réalisable en 90 minutes

🎯 Objectif : 

> Pouvoir dire en entretien :
> “J’ai monté une petite API TypeScript connectée à PostgreSQL.”

Même simple, c’est très crédible.

---

### Étape 1

Installer Node.js. : [ici](https://nodejs.org)

---

### Étape 2

Créer un projet
```
mkdir api-test
cd api-test
npm init -y
```

---

### Étape 3

Installer Express
```
npm install express
```

Express est un framework backend très utilisé.

---

### Étape 4

Créer un fichier `server.js`

Exemple minimal :
```
const express = require('express')

const app = express()

app.get('/users', (req, res) => {
  res.json([
    { id: 1, name: "Alice" },
    { id: 2, name: "Bob" }
  ])
})

app.listen(3000, () => {
  console.log("API running on port 3000")
})
```

---

### Étape 5

Lancer le serveur
```
node server.js
```

Tester dans le navigateur :
```
http://localhost:3000/users
```

---

### Étape 6

Option bonus : PostgreSQL

Installer PostgreSQL : [ici](https://www.postgresql.org)

Créer une table :

```
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT
);
```

---

## 🔼 Outro :

### 📢 Comment présenter ça en entretien

Exemple de formulation simple :
> “Je me suis formé aux bases d’une stack TypeScript / Node / PostgreSQL et j’ai réalisé un petit prototype d’API REST pour comprendre comment un backend dialogue avec une base de données et comment ces services sont ensuite déployés dans le cloud.”

Cette phrase montre :
* compréhension
* initiative
* autonomie

---

## ☝️ Point important pour la promo

Le recruteur ne cherche probablement pas :

❌ un développeur expert

Il cherche plutôt :

* quelqu’un qui apprend vite
* capable d’utiliser l’IA comme outil
* mais **qui comprend l’architecture logicielle**


# :package: **Kit de préparation d'entretien**

Voici un kit très concret pour préparer un entretien sur ce type de stack.
L’idée n’est pas de devenir développeur en une semaine, mais d’éviter les réponses naïves et de **montrer une compréhension structurée**.

--- 

## :one: **Définitions principales**

### :point_right: TypeScript

> TypeScript est une extension de JavaScript qui ajoute un système de types. Cela permet de détecter des erreurs avant l’exécution et rend le code plus robuste dans les projets complexes.

---

### :point_right: API REST

> Une API REST est une interface qui permet à des applications de communiquer via des requêtes HTTP. Elle expose des endpoints qui permettent de lire ou modifier des données.

---

### :point_right: JSON

> JSON est un format de données simple utilisé pour échanger des informations entre un client et un serveur.

---

### :point_right: PostgreSQL

> PostgreSQL est une base de données relationnelle très utilisée pour stocker des données structurées et effectuer des requêtes SQL.

---

### :point_right: AWS

> AWS est une plateforme cloud qui permet d’héberger des applications, des bases de données et des services sans gérer directement les serveurs physiques.

---

## :two: Les 20 questions techniques probables

Ce sont des questions **très fréquentes pour des profils juniors / alternance** sur ce type de stack.

### :point_right: JavaScript / TypeScript

1. Quelle est la différence entre JavaScript et TypeScript ?
2. Pourquoi utiliser TypeScript dans un projet ?
3. Qu’est-ce qu’un type ou une interface ?
4. Que fait `async / await` ?
5. Quelle est la différence entre `let`, `const` et `var` ?

---

### :point_right: Backend / API

6. Qu’est-ce qu’une API REST ?
7. Que signifie un endpoint ?
8. Quelle différence entre `GET` et `POST` ?
9. À quoi sert JSON dans une API ?
10. Qu’est-ce que le backend dans une application web ?

---

### :point_right: Base de données

11. Qu’est-ce qu’une table dans une base de données ?
12. Qu’est-ce qu’une clé primaire ?
13. Pourquoi indexer une base ?
14. À quoi sert SQL ?
15. Pourquoi utiliser PostgreSQL ?

---

### :point_right: Cloud

16. Pourquoi utiliser le cloud plutôt qu’un serveur local ?
17. À quoi sert Amazon Web Services ?
18. Quelle différence entre stockage et base de données ?
19. Qu’est-ce qu’un serveur ?
20. Qu’est-ce que le déploiement d’une application ?

---

## ➡️ Réponses

### 👉 JavaScript / TypeScript

-

* *1. Quelle différence entre JavaScript et TypeScript ?*
> TypeScript est une extension de JavaScript qui ajoute un système de typage statique. Le code TypeScript est ensuite compilé en JavaScript avant d’être exécuté.

---

* *2. Pourquoi utiliser TypeScript ?*
> Le typage permet de détecter certaines erreurs avant l’exécution et rend le code plus lisible et plus robuste dans les projets importants.

---

* *3. Qu’est-ce qu’un type ou une interface ?*
> Un type décrit la forme que doivent avoir des données (par exemple un utilisateur avec un id et un nom). Cela permet de garantir que les fonctions utilisent des données conformes à cette structure.

---

* *4. Que fait `async / await` ?*
> `async / await` permet d’écrire du code asynchrone de manière lisible, en attendant le résultat d’une opération longue (appel API, base de données) sans bloquer le programme.

---

* *5. Différence entre `let`, `const` et `var`*
> `var` est l’ancienne manière de déclarer des variables. `let` permet de modifier la variable, alors que `const` indique qu’elle ne doit pas être réassignée.

---

### 👉 Backend / API

-

* *6. Qu’est-ce qu’une API REST ?*
> Une API REST est une interface qui permet à des applications de communiquer via des requêtes HTTP pour lire ou modifier des données.

---

 * *7. Qu’est-ce qu’un endpoint ?*
> Un endpoint est une URL spécifique d’une API qui permet d’effectuer une action, par exemple récupérer ou créer des données.
> 
> Exemple : ```GET /users```

---

* *8. Différence entre `GET` et `POST`*
> `GET` sert à récupérer des données.
> `POST` sert à envoyer des données pour créer une ressource.

---

* *9. À quoi sert JSON ?*
> JSON est un format de données simple utilisé pour échanger des informations entre un client et un serveur.

---

* *10. Qu’est-ce que le backend ?*
> Le backend est la partie serveur d’une application qui gère la logique métier, les API et l’accès aux bases de données.

---

### 👉 Base de données

-

* *11. Qu’est-ce qu’une table ?*
> Une table est une structure qui organise les données en lignes et colonnes dans une base de données.

---

* *12. Qu’est-ce qu’une clé primaire ?*
> Une clé primaire est un identifiant unique qui permet de distinguer chaque ligne d’une table.

---

* *13. Pourquoi utiliser un index ?*
> Un index permet d’accélérer les recherches dans une base de données en évitant de parcourir toute la table.

---

* *14. À quoi sert SQL ?*
> SQL est un langage utilisé pour interroger et modifier les données dans une base de données relationnelle.
> 
> Exemple : ```SELECT * FROM users```

---

* *15. Pourquoi utiliser PostgreSQL ?*
> PostgreSQL est une base de données relationnelle robuste, open source et très utilisée dans les applications web et SaaS.

---

### 👉 Cloud

-

* *16. Pourquoi utiliser le cloud ?*
> Le cloud permet d’héberger des applications et des bases de données sans gérer directement l’infrastructure physique.

---

* *17. À quoi sert AWS ?*
> AWS fournit des services cloud pour héberger des serveurs, des bases de données, du stockage et des applications.

---

* *18. Différence entre stockage et base de données
> Le stockage conserve des fichiers (images, documents).
> Une base de données organise et interroge des données structurées.

---

* *19. Qu’est-ce qu’un serveur ?*
> Un serveur est une machine qui fournit des services ou des données à d’autres machines via un réseau.

---

* *20. Qu’est-ce que le déploiement d’une application ?*
> Le déploiement consiste à installer et rendre accessible une application sur une infrastructure (serveur ou cloud).

---

## 3️⃣ Les 10 erreurs classiques des candidats débutants

Les recruteurs techniques les voient constamment.

### ❌ 1. Mélanger frontend et backend

Frontend = interface
Backend = logique serveur

---

### ❌ 2. Confondre API et base de données

API = programme qui manipule les données
Base = stockage

---

### ❌ 3. Penser que TypeScript remplace JavaScript

TypeScript **compile vers JavaScript**.

---

### ❌ 4. Ne pas comprendre HTTP

`GET` = lire
`POST` = créer
`PUT` = modifier
`DELETE` = supprimer

---

### ❌ 5. Dire “je sais coder” sans exemple

Même un mini-projet simple vaut mieux.

---

### ❌ 6. Ne pas comprendre les erreurs

Une erreur fait partie du développement.

---

### ❌ 7. Copier du code IA sans comprendre

C’est précisément ce que critique souvent le “vibe coding”.

---

### ❌ 8. Ignorer la structure du projet

Les recruteurs regardent si vous comprenez **l’architecture**.

---

### ❌ 9. Ne pas poser de questions techniques

Un bon candidat demande :

* comment est organisée l’API
* comment sont gérées les données
* comment le projet est déployé

---

### ❌ 10. Croire qu’on attend un expert

Pour une alternance, on cherche surtout :

* curiosité
* capacité d’apprentissage
* rigueur


## 4️⃣ Conseils stratégiques pour votre promo

### 👉 Le message de l’employeur

> “Profil qui croit au vibe coding structuré”

signifie probablement :
* utiliser l’IA pour accélérer le développement
* **mais garder une discipline d’ingénierie**

Donc ce qu’il veut vérifier en entretien :
* est-ce que vous comprenez la stack
* est-ce que vous savez apprendre vite
* est-ce que vous comprenez ce que vous codez

---

### 👉 Pour des profils non-dev
-

Un bon positionnement peut être :

> “Je ne viens pas d’un parcours de développeur, mais j’ai voulu comprendre comment fonctionne une architecture TypeScript / API / base de données afin d’être capable de dialoguer efficacement avec des équipes techniques.”

C’est **très crédible pour un futur chef de projet technique**.

---

### 👉 La clé de l'entretien
-

La clé en entretien n’est pas la technicité mais **la cohérence** :
> Comprendre l’architecture générale d’une application web.

Expliquer simplement :
```
utilisateur
→ frontend
→ API backend
→ base de données
→ cloud```
suffit souvent à montrer que vous comprenez la logique du système.

---