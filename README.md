# SPEAK NOW v2.1 — MVP CONNECTÉ

Version indépendante et refondue. Elle ajoute une vraie couche serveur aux principales fonctions du MVP :
- comptes / connexion JWT
- PostgreSQL
- langues actives (maximum 4)
- cours et progression enregistrés en base
- XP et série
- recherche d’utilisateurs
- demandes d’amis
- chat privé avec contrôle d’accès
- blocage et signalement
- notifications
- SPEAK AI via endpoint backend

## Installation
1. Installer Docker Desktop et Node.js.
2. `docker compose up -d`
3. `cd backend && npm install`
4. Copier `.env.example` vers `.env` et définir `JWT_SECRET`.
5. Optionnel pour la vraie correction IA : renseigner `OPENAI_API_KEY`.
6. `node server.js`
7. Ouvrir `frontend/index.html`.

API : http://localhost:3000

## SPEAK AI
Le backend utilise l’OpenAI Responses API lorsque `OPENAI_API_KEY` est configurée. Le modèle est configurable avec `OPENAI_MODEL` et prend par défaut `gpt-5.6-luna`.

Ne mets jamais la clé API dans le frontend.

## Important
Cette version est un MVP de développement, pas encore une mise en production publique. Avant publication : HTTPS, gestion sécurisée des secrets, validation renforcée, rate limiting, modération et supervision.


## TEST RAPIDE DU SERVEUR

### 1. Démarrer PostgreSQL
```bash
docker compose up -d
```

### 2. Démarrer l'API
```bash
cd backend
npm install
node server.js
```

L'API doit écouter sur `http://localhost:3000`.

### 3. Tester depuis SPEAK NOW
Ouvre `frontend/index.html`, indique `http://localhost:3000`, puis clique sur **Tester le serveur**.

Si tu obtiens « Serveur connecté », le frontend communique bien avec l'API.
