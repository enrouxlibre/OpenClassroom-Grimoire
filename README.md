# Mon Vieux Grimoire / Grimoire

## An OpenClassroom Web Development Project

---

## Français

### À propos du projet

**"Mon Vieux Grimoire"** est un projet web complet développé dans le cadre de la formation **Web Developer** d'OpenClassroom. Il s'agit d'une application de gestion de livres avec un système de notation et d'authentification utilisateur.

### Architecture

Le projet est composé de trois parties :

- **Frontend** : Application React avec interface utilisateur moderne
- **Backend** : API Node.js/Express avec système d'authentification
- **Base de données** : MongoDB (facilement déployable avec Docker)

### Fonctionnalités

- Gestion complète des livres (création, modification, suppression)
- Système de notation des livres
- Authentification et gestion des utilisateurs
- Protection des routes avec JWT
- Upload et optimisation d'images
- Interface responsive

### Prérequis

- Node.js (version 16 ou supérieure)
- npm ou yarn
- MongoDB (installé localement ou via Docker)
- Docker et Docker Compose (pour utiliser la base de données conteneurisée)

### Installation et démarrage

#### 1. Cloner le projet

```bash
git clone <url-du-repo>
cd Grimoire
```

#### 2. Configurer les variables d'environnement

Créer un fichier `.env` à la racine du projet :

```env
MONGO_INITDB_ROOT_USERNAME=admin
MONGO_INITDB_ROOT_PASSWORD=password
JWT_SECRET=RANDOM_TOKEN_SECRET
```

#### 3. Installation des dépendances

**Backend** :

```bash
cd backend
npm install --force
```

**Frontend** :

```bash
cd frontend
npm install --force
```

#### 4. Démarrer l'application

**Option 1 : Avec Docker Compose**

```bash
docker-compose up
```

**Option 2 : Manuellement**

Terminal 1 (Backend) :

```bash
cd backend
npm start
```

Terminal 2 (Frontend) :

```bash
cd frontend
npm start
```

### Technologies utilisées

**Backend** :

- Node.js
- Express.js
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- Multer
- Sharp

**Frontend** :

- React
- React Router
- CSS Modules

---

## Educational Context

This project is part of the OpenClassroom Web Developer course and demonstrates:

- Full-stack web development
- RESTful API design
- Database integration and management
- User authentication and authorization
- Front-end and back-end separation
- Modern web development practices

## Démarrage du projet

### Option 1 : Avec Docker (recommandé)

**Prérequis** : Docker et Docker Compose installés

```bash
# À la racine du projet
docker-compose up --build
```

Les services seront accessibles sur :

- Frontend : http://localhost:3000
- Backend : http://localhost:4000
- MongoDB : localhost:27017

### Option 2 : Démarrage manuel

#### 1. Démarrer MongoDB

Si MongoDB n'est pas lancé sur Docker :

```bash
docker-compose up
```

#### 2. Démarrer le backend

```bash
cd backend
npm start
```

Le serveur backend sera accessible sur http://localhost:4000

#### 3. Démarrer le frontend

Dans un nouveau terminal :

```bash
cd frontend
npm start
```

L'application React sera accessible sur http://localhost:3000

## Structure du projet

```
grimoire/
├── backend/
│   ├── controllers/      # Contrôleurs pour la logique métier
│   ├── middleware/       # Middleware d'authentification et upload
│   ├── models/           # Modèles Mongoose
│   ├── routes/           # Routes de l'API
│   ├── images/           # Dossier de stockage des images
│   ├── app.js            # Configuration Express
│   └── server.js         # Point d'entrée du serveur
├── frontend/
├── .env                  # Variables d'environnement
└── docker-compose.yml    # Configuration Docker Compose
```

## API Endpoints

### Authentification

- `POST /api/auth/signup` - Créer un compte utilisateur
- `POST /api/auth/login` - Se connecter

### Livres

- `GET /api/books` - Récupérer tous les livres
- `GET /api/books/:id` - Récupérer un livre par ID
- `POST /api/books` - Créer un livre (authentification requise)
- `PUT /api/books/:id` - Modifier un livre (authentification requise)
- `DELETE /api/books/:id` - Supprimer un livre (authentification requise)
- `POST /api/books/:id/rating` - Noter un livre (authentification requise)
- `GET /api/books/bestrating` - Récupérer les 3 livres les mieux notés

## Technologies utilisées

### Backend

- Node.js
- Express.js
- MongoDB avec Mongoose
- mongoose-unique-validator pour s'assurer que les e-mail sont uniques
- JWT pour l'authentification
- Multer pour l'upload d'images
- bcrypt pour le hashage des mots de passe
