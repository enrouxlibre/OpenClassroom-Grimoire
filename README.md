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
