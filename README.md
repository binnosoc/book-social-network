# Book Social Network

**Book Social Network** est une application full-stack permettant aux utilisateurs de gérer leurs collections de livres et d'interagir avec une communauté de passionnés de lecture.

## Objectif du Projet

L'application offre les fonctionnalités suivantes :

- **Gestion des utilisateurs** : Inscription des utilisateurs avec validation sécurisée par email.
- **Gestion des livres** : Création, mise à jour, partage et archivage de livres.
- **Emprunt et retour de livres** : Vérification de la disponibilité des livres pour l'emprunt et gestion des retours avec approbation.
- **Sécurité** : Utilisation de tokens JWT pour l'authentification et l'autorisation, respectant les meilleures pratiques de conception d'API REST.

## Fonctionnalités

### Sécurité de l'API

L'API utilise **Spring Boot** et **Spring Security** pour garantir une sécurité robuste à travers l'utilisation de **JWT (JSON Web Tokens)** :

1. **Requêtes HTTP** : Les utilisateurs envoient des requêtes HTTP de différents types (GET, POST, PATCH, DELETE).
2. **Chaîne de filtres** : Les requêtes passent par une chaîne de filtres (authentification, journalisation, etc.) avant d'atteindre les contrôleurs.
3. **JwtAuthenticationFilter** : Un filtre spécifique pour extraire et valider le JWT par `JwtService`.
4. **UserDetailsService** : Chargement des détails de l'utilisateur depuis la base de données si le token est valide.
5. **SecurityContextHolder** : Stockage des détails de l'utilisateur authentifié pour gérer l'authentification et l'autorisation.
6. **DispatcherServlet et Contrôleurs** : Le `DispatcherServlet` dirige la requête vers le contrôleur approprié pour traitement.

### Architecture de l'API

L'architecture de l'API est organisée en plusieurs couches :

- **Controller** : Reçoit les requêtes HTTP et renvoie une réponse après traitement.
- **Service** : Contient la logique métier de l'application.
- **DTO (Data Transfer Object)** : Transfère les données entre les différentes couches.
- **DAO (Data Access Object)** : Gère l'accès aux données dans la base de données.
- **Base de données** : Stocke les données persistantes de l'application.

## Technologies Utilisées

- **Langage de programmation** : Java 21
- **Frameworks** : Spring Boot 3
- **Base de données** : PostgreSQL
- **Type de projet** : Maven
- **Packaging** : JAR
- **Conteneurisation** : Docker

### Principales Dépendances Intégrées

- Spring Data JPA
- Spring Web
- Lombok
- Spring Security 6
- JWT Token Authentication
- OpenAPI et Documentation UI de Swagger
- Java Mail Sender
- JSR-303 et Spring Validation
- Spring Boot DevTools
- Keycloak

## Détails du Projet

Le projet est une application robuste et sécurisée utilisant les dernières technologies pour offrir une expérience utilisateur optimale.

## Code Source

Le code source de l'application est disponible sur GitHub : [Book Social Network](https://github.com/binnosoc/book-social-network).

## Auteur

Développé par **[Ousseni BORO]**.

