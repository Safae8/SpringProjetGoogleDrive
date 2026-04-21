# Application Google Drive Clone

Ce projet est une application Full Stack de gestion de fichiers, inspirée de Google Drive. Elle permet aux utilisateurs de stocker, gérer et partager leurs fichiers de manière sécurisée en utilisant une architecture robuste basée sur Spring Boot pour le backend et Angular pour le frontend.

##  Lien du Repository GitHub

 **[Lien vers votre repository GitHub ici]** *(https://github.com/Safae8/SpringProjetGoogleDrive.git)*

---

##  Fonctionnalités Principales

- **Authentification et Sécurité** : 
  - Connexion via des identifiants classiques (Email/Mot de passe) sécurisée par JWT (JSON Web Tokens).
  - Intégration de l'authentification **Google OAuth2** (Single Sign-On).
- **Gestion des Fichiers et Dossiers** : 
  - Upload (téléversement) de fichiers vers le serveur.
  - Organisation des fichiers dans des dossiers.
  - Téléchargement, renommage et suppression de fichiers/dossiers.
  - Gestion de la visibilité des fichiers : publics et privés.
  -  Les fichiers privés nécessitent une autorisation explicite du propriétaire pour être téléchargés.
- **Interface Utilisateur Moderne** : 
  - Interface intuitive et responsive développée avec Angular et Angular Material.

---

##  Technologies Utilisées

### Backend (Dossier `ApplicationGoogleDrive`)
- **Framework** : Spring Boot 4.0.0
- **Langage** : Java 17
- **Base de données** : MySQL
- **Sécurité** : Spring Security, JWT, OAuth2 Client
- **ORM** : Spring Data JPA / Hibernate
- **Utilitaires** : Lombok, Maven

### Frontend (Dossier `frontend`)
- **Framework** : Angular 19
- **Langage** : TypeScript
- **UI/UX** : Angular Material
- **Authentification** : @auth0/angular-jwt

---

##  Comment lancer le projet localement ?

### Prérequis
Avant de commencer, assurez-vous d'avoir installé :
- **Java 17** (JDK)
- **Node.js** (version 18+ recommandée) et **npm**
- **MySQL Server**
- **Maven** (Optionnel, le wrapper `mvnw` est inclus)
- **Angular CLI** (`npm install -g @angular/cli`)

### 1. Configuration de la Base de données
1. Lancez votre serveur MySQL.
2. Créez une base de données pour l'application (vérifiez le nom exact dans `ApplicationGoogleDrive/src/main/resources/application.properties`, par exemple `drive_db`).
3. Assurez-vous que les identifiants MySQL (username et password) correspondent à ceux configurés dans le fichier `application.properties`.

### 2. Démarrer le Backend (Spring Boot)
1. Ouvrez un terminal et naviguez dans le dossier du backend :
   ```bash
   cd ApplicationGoogleDrive
   ```
2. Vérifiez ou configurez les variables d'environnement dans le fichier `.env` (Google Client ID, Secret, JWT Secret).
3. Compilez et lancez l'application :
   - Sous Windows : `mvnw.cmd spring-boot:run`
   - Sous Mac/Linux : `./mvnw spring-boot:run`
4. Le backend démarrera généralement sur `http://localhost:8080`.

### 3. Démarrer le Frontend (Angular)
1. Ouvrez un nouveau terminal et naviguez dans le dossier du frontend :
   ```bash
   cd frontend
   ```
2. Installez les dépendances Node.js :
   ```bash
   npm install
   ```
3. Lancez le serveur de développement Angular :
   ```bash
   ng serve
   ```
4. Ouvrez votre navigateur et accédez à l'application via `http://localhost:4200`.

---

## 📂 Structure du projet

```
├── ApplicationGoogleDrive/  # Code source du backend Spring Boot
│   ├── src/                 # Contrôleurs, Services, Repositories, Modèles
│   ├── .env                 # Variables d'environnement (clés API, secrets)
│   └── pom.xml              # Dépendances Maven
├── frontend/                # Code source du frontend Angular
│   ├── src/                 # Composants, Services, Routes, Styles
│   └── package.json         # Dépendances Node.js
└── uploads/                 # Dossier de stockage des fichiers téléversés
```
